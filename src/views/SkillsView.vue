<script setup lang="ts">
import type { ISkill } from '@/interfaces';
import axios from 'axios';

const skills: ISkill[] = (
    await axios.get('https://edwardtanguay.vercel.app/share/skills.json')
).data;
</script>
 
<template>
  <div class="skills">
    <h2>Skills</h2>
    <p>There are {{ skills.length }} skills.</p>
    <ul>
      <li v-for="skill in skills">
        <a target="_blank" :href="skill.url">{{ skill.name }}</a> - {{ skill.description }}
      </li>
    </ul>
  </div>
</template>
 
<style scoped>
.skills {
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