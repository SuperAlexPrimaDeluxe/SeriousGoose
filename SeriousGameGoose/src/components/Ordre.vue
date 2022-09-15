<script setup>
  //import {defineProps} from 'vue'
    import "/style.css";
    const props = defineProps(['thequestion'])
    </script>
    
    <template>
      <div class="ordre-question">
         <h3>{{ thequestion.question }}</h3>
      </div>
    </template>
    
    <style scoped>

  </style>