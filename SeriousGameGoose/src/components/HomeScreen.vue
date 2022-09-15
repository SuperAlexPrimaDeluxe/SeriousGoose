

<script setup>
    import {ref, computed} from 'vue'
    import { useGameStore } from '@/stores/game';
    import Joueur from '@/components/Joueur.vue';
    import { RouterLink, RouterView } from "vue-router";
   
   
  
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
       <div class="wrapper">
    <header>
      <input type="text" v-model="newUser"> <button @click="addUser">Ajouter un joueur</button>
      <br /><br />
   
        <Joueur v-for="(item, key) in listMembers" :key="key" :ident="key"></Joueur>
      <Plateau />
    </header>
  </div>
  </template>
  
