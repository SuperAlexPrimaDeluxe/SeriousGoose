<script>
    export default {
      data() {
        return {
          picked: 2,
          awesome: false,
          team1: "",
          team2: "",
          team3: "",
          team4: "",
          team5: "",
        };
      },
    };
    </script>
    
    <template>
      <div>Nombre de joueur / équipe : {{ picked }}</div>
    
      <input
        type="radio"
        id="two"
        value="2"
        v-model="picked"
        @click="awesome = !awesome"
      />
      <label for="two">2</label>
    
      <input type="radio" id="three" value="3" v-model="picked" />
      <label for="three">3</label>
    
      <input type="radio" id="four" value="4" v-model="picked" />
      <label for="four">4</label>
    
      <input type="radio" id="five" value="5" v-model="picked" />
      <label for="four">5</label>
    
      <br /><br />
    
      <label for="team1">Nom du joueur / équipe 1 : </label>
      <input v-model="team1" type="text" id="team1" name="team1" /><br />
      <h3>Le nom de votre équipe est : {{ team1 }}</h3>
    
      <label for="team2">Nom du joueur / équipe 2 : </label>
      <input v-model="team2" type="text" id="team2" name="team2" /><br />
      <h3>Le nom de votre équipe est : {{ team2 }}</h3>
    
      <div v-if="picked > 2">
        <label for="team3">Nom du joueur / équipe 3 : </label>
        <input v-model="team3" type="text" id="team3" name="team3" /><br />
        <h3>Le nom de votre équipe est : {{ team3 }}</h3>
      </div>
    
      <div v-if="picked > 3">
        <label for="team4">Nom du joueur / équipe 4 : </label>
        <input v-model="team4" type="text" id="team4" name="team4" /><br />
        <h3>Le nom de votre équipe est : {{ team4 }}</h3>
      </div>
      <div v-if="picked > 4">
        <label for="team5">Nom du joueur / équipe 5 : </label>
        <input v-model="team5" type="text" id="team5" name="team5" /><br />
        <h3>Le nom de votre équipe est : {{ team5 }}</h3>
      </div>
      <button>Commencer le jeu</button>
    </template>
    
    