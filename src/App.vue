<script setup lang="ts">
import { onErrorCaptured, ref, } from 'vue'
import { RouterLink, RouterView } from 'vue-router/auto'

onErrorCaptured((err, instance, info) => {
  console.error('erreur : ', err, '\ninfo : ', info, '\ncomposant : ', instance)
  return true
})
const menuIsOpen = ref(false)
</script>

<template>
  <header>
    <button
      aria-controls="mainNav"
      aria-expanded="true"
      class="rounded-full border-2 border-red-600 bg-red-300 px-2"
      @pointerdown="menuIsOpen = !menuIsOpen"
    >
      menu
    </button>
    <Transition
  class="transition-transform duration-1000"
  enter-from-class="-translate-x-full"
  enter-to-class="translate-x-0"
  leave-active-class="-translate-x-full"
  >
    <nav id="mainNav" v-show="menuIsOpen">
      <ul>
        <li><RouterLink to="/" class="text-red-500 underline"> Accueil </RouterLink></li>
        <li><RouterLink to="/donnees" class="text-red-500 underline"> Données </RouterLink></li>
        
      </ul>
    </nav>
  </Transition>

    <nav>
      <ul>
        <li>
          
        </li>
      </ul>
    </nav>
  </header>
  <RouterView v-slot="{ Component }">
    <Suspense>
      <component :is="Component" />
    </Suspense>
  </RouterView>
</template>
