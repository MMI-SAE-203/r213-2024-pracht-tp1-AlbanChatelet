<script setup lang="ts">
  import { ref } from 'vue';

  const sectionsData = [
    {
      label: 'bouton 1',
      texte: `texte panneau 1 Lorem ipsum dolor sit ame
      consectetur adipisicing elit. Inventore animi dolore,
      rerum magni laudantium quod excepturi laboriosam, 
      ex modi debitis harum reprehenderit eaque quam ut
      ea molestiae. Id, cum dolor!`,
      isOpen: ref(false)
    },
    {
      label: 'bouton 2',
      texte: `texte panneau 2 Amet alias provident quos quis, 
      Officia ut ab dolores quos dolorem accusamus ad,
      consectetur unde minima, ipsum eligendi inventore id
      labore, laborum rerum laboriosam corrupti iste.
      Distinctio, perspiciatis!`,
      isOpen: ref(false)
    },
    {
      label: 'bouton 3',
      texte: `texte panneau 3 Repudiandae corporis voluptates, 
      odit reprehenderit sint pariatur at voluptatum, cumque
      quia sit eligendi ex culpa eos, alias magnam molestiae
      id modi accusantium ipsa eveniet accusamus. Tempora 
      quis corporis et nam.`,
      isOpen: ref(false)
    }
  ]
</script>

<template>
  <h1>Données</h1>
  <section v-for="(section, key) of sectionsData" :key="key">
    <button class="text-xl" @pointerdown="toggleSection(key)">{{ section.label }}</button>
    <p v-show="section.isOpen">{{ section.texte }}</p>
  </section>
</template>

<script lang="ts">
  const toggleSection = (key: number) => {
    sectionsData[key].isOpen.value = !sectionsData[key].isOpen.value;
  };
</script>


