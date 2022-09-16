<script setup>
  //import {defineProps} from 'vue'
    import "/style.css";
    const props = defineProps(['thequestion'])
    </script>
    
    <template>
   <div class="cadre">
    <h3>La question est</h3>
    <div class="blokito">
    <input type="text" />
    <button>Valider la réponse</button>
  </div>
  </div>
    </template>
    
    