<script setup lang="ts">
import TeamMemberItem from '@/components/TeamMemberItem.vue';
import type { TeamMember } from '@/shared/types';
const teamMembers: TeamMember[] = [
  {
    id: 1,
    name: 'Viktor Baran',
    position: 'Frontend Developer',
    image: 'https://avatars.githubusercontent.com/u/125183903?v=4',
  },
  {
    id: 2,
    name: 'Danylo Savytskyi',
    position: 'Project Manager',
    image: 'https://avatars.githubusercontent.com/u/107762418?s=400&u=b1347f293f12a1399ada2731cad8610890be2375&v=4',
  },
  {
    id: 3,
    name: 'Oleksandr Suslov',
    position: 'Web Designer',
    image: 'https://avatars.githubusercontent.com/u/113384549?v=4',
  },
  {
    id: 4,
    name: 'Suslova Anna',
    position: 'QA Engineer',
    image: 'https://avatars.githubusercontent.com/u/51747613?v=4',
  },
  {
    id: 5,
    name: 'Vlad Snisar',
    position: 'Placeholder',
    image: 'https://avatars.githubusercontent.com/u/85521093?v=4',
  }
];
</script>

<template>
  <main class="root">
    <div class="members">
      <div v-for='teamMember in teamMembers' :key='teamMember.id'>
        <TeamMemberItem :teamMember=teamMember />
      </div>
    </div>
  </main>
</template>

<style scoped>
.root {
  display: flex;
  justify-content: center;
  align-items: center;
}
.members {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 60rem;
  gap: 1rem;
}
</style>
