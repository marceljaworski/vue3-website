<script setup lang="ts">
import type { IJob } from '@/interfaces';
import axios from 'axios';

const jobs: IJob[] = (await axios.get('https://edwardtanguay.vercel.app/share/jobs.json')).data;
 

</script>
<template>
  <div class="jobs">
    <h2>This is an Vue3 boilerplate / jobs view</h2>
    <p>There are {{ jobs.length }} jobs.</p>
  </div>
</template>
