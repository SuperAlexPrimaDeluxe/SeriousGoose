<script>
    import "/style.css";
    
    import Joueur from "@/components/Joueur.vue";
    import Dice from "@/components/Dice.vue";
    import Formmultiple from "@/components/Formmultiple.vue";
    import axios from "axios";

    
    export default {
      data() {
        return {
          posts: [],
        };
      },
      components: {
    Dice,
    Joueur,
    Formmultiple
},
      mounted() {
        axios
          .get(
            "https://killer-cepegra.xyz/cockpit-ingrwf10/api/content/items/questions?sort=%7Bnumber%3A%22asc%22%7D"
          )
          .then((response) => {
            //this.posts = response.data;
            console.log(response.data);
            this.posts = response.data; // dans mon tableau
          });
      },
    };
    </script>
    
    <template>
      <div>
        <Joueur></Joueur>
        <Dice></Dice>
        <div className="de" v-for="(question, key) in posts" :key="key">
          {{ question.number }}
          <Formmultiple v-if="question && question.qtype =='form-multiple'">
            <h3>zbub</h3>
          </Formmultiple>
        </div>
      </div>
    </template>
    
    