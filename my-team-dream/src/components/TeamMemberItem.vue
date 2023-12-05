<script setup lang='ts'>
import type { TeamMember } from '@/shared/types';

defineProps<{
  teamMember: TeamMember;
}>()
const getPositionColor = (id: number): string => {
  if (id === 1) {
    return 'blue';
  } else if (id === 2) {
    return 'green';
  } else if (id === 3){
    return 'magenta';
  } else if (id === 4){
    return 'orange';
  } else {
    return 'red';
  }
};
</script>

<template>
  <main>
    <h1>{{ teamMember.name }}</h1>
    <p :style="{ color: getPositionColor(teamMember.id) }">{{ teamMember.position }} 😎</p>
    <img :src='teamMember.image' :alt='teamMember.name' />
  </main>
</template>

<style scoped>
main {
  background-color: var(--color-background-mute);
  border-radius: 1rem;
  padding: 1.5rem;
  width: 18rem;
  transition: scale .3s ease-in-out;
  text-align: center;
}

main:hover {
  background-color: var(--color-background-soft);
  scale: 1.05;
}


h1 {
  font-size: 1.5rem;
  margin: 0;
  color: var(--color-heading);
  font-weight: bold;
}

p {
  font-size: 1rem;
  margin: 0;
  color: var(--color-text);
  font-weight: bold;
}

img {
  border-radius: 50%;
  width: 12rem;
  aspect-ratio: 1 / 1;
  padding: 1rem;
}

</style>
