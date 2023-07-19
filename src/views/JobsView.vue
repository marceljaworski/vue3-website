<script setup lang="ts">
import type { IJob } from '@/interfaces';
import axios from 'axios';

const jobs: IJob[] = (await axios.get('https://edwardtanguay.vercel.app/share/jobs.json')).data;
 

</script>
<template>
  <div class="jobs">
    <h2>Jobs</h2>
    <p>There are {{ jobs.length }} jobs.</p>
    <ul>
      <li v-for="job in jobs">
        <a target="_blank" :href="job.url">{{ job.title }}</a> - {{ job.company }}</li>
    </ul>
  </div>
</template>

<style scoped>
.jobs {
  margin: auto;
  max-width: 700px;
  padding-inline: 1rem;
}
h2 {
  color: rgb(255, 200, 0);
}
 
p {
  color: #aaa;
  font-style: italic;
  text-align: left;
}

li {
  color: #ccc;
  font-size: 1.3rem;
  text-align: left;
}
a {
  color: rgb(47, 106, 255);
}
</style>