<script setup>
  //import {defineProps} from 'vue'
    import "/style.css";
    const props = defineProps(['thequestion'])
    </script>
    
    <template>
      <div>
        <div>
         <p>{{ thequestion.question }}</p>
        </div>
      </div>
    </template>
    
    