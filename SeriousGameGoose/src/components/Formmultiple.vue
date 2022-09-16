<script setup>
  //import {defineProps} from 'vue'
    import "/style.css";
    const props = defineProps(['thequestion'])
    </script>
    
    <template>
   <div class="cadre">
    <h3>La question est</h3>
    <div class="blokito">
    <fieldset>
    <legend>Sélectionnez votre réponse</legend>

    <div>
      <input type="radio" id="huey" name="drone" value="huey"
             checked>
      <label for="huey">Réponse 1</label>
    </div>

    <div>
      <input type="radio" id="dewey" name="drone" value="dewey">
      <label for="dewey">Réponse 2</label>
    </div>

    <div>
      <input type="radio" id="louie" name="drone" value="louie">
      <label for="louie">Réponse 3</label>
    </div>
</fieldset>
<button> Valider la réponse </button>
  </div>
  </div>
    </template>
    
    