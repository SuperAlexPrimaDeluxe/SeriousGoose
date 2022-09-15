

<script setup>
  import {ref, computed} from 'vue'
  import { useGameStore } from '@/stores/game';
  import Joueur from '@/components/Joueur.vue';
  import { RouterLink, RouterView } from "vue-router";
  import Plateau from "@/components/Plateau.vue";
  import Formmultiple from "@/components/Formmultiple.vue";

  const gameStore = useGameStore()
  const members = ['Pierre', 'Jean', 'Charles']
  gameStore.addMembers(members)
  const listMembers = computed( () => { return gameStore.allJoueurs})
  const newUser = ref('')
  const addUser = () => {
    gameStore.addAMember(newUser.value)
  }
  </script>

<template>
<Plateau />
</template>

