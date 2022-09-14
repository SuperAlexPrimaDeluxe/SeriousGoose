<script setup>
    import { useGameStore } from '@/stores/game'
    const gameStore = useGameStore()
    const props = defineProps(['ident'])
    const theJoueur = gameStore.oneJoueur(props.ident)
</script>
    
<template>
    <h1>Joueur :{{ident}} est : {{theJoueur}}</h1>
</template>
    
    