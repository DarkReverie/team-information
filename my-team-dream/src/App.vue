<script setup lang="ts">
import TeamMemberItem from '@/components/TeamMemberItem.vue';
import type { TeamMember } from '@/shared/types';

const teamMembers: TeamMember[] = [
  {
    id: 1,
    name: 'Viktor Baran',
    position: 'Project Manager',
    image: 'https://avatars.githubusercontent.com/u/125183903?v=4',
  },
  {
    id: 3,
    name: 'Vlad Snisar',
    position: 'BackEnd Developer',
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
