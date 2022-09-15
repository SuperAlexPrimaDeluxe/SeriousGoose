<script setup>
  //import {defineProps} from 'vue'
    import "/style.css";
    const props = defineProps(['thequestion'])
    </script>
    
    <template>
      <div>
        <div>
         <h3>{{ thequestion.question }}</h3>
        </div>
      </div>
    </template>
    
    <style scoped>

  </style>