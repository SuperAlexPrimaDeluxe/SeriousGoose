<script setup>
  //import {defineProps} from 'vue'
    import "/style.css";
    const props = defineProps(['thequestion'])
    </script>
    
    <template>
  <div class="cadre">
    <h3>Composant Liaison </h3>
    <div class="blokito">
    <div class="bloc1">
      <ul>
        <li>La réponse possible une</li>
        <li>La réponse possible deux</li>
        <li>La réponse possible trois</li>
      </ul>
    </div>
    <div class="bloc2">
  <select name="cars" id="cars">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="mercedes">Mercedes</option>
  <option value="audi">Audi</option>
</select>
<select name="cars" id="cars">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="mercedes">Mercedes</option>
  <option value="audi">Audi</option>
</select>
<select name="cars" id="cars">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="mercedes">Mercedes</option>
  <option value="audi">Audi</option>
</select>
    </div>
  </div>
  </div>
    </template>
    