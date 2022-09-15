<script>
    import "/style.css";
    
    import Joueur from "@/components/Joueur.vue";
    import Dice from "@/components/Dice.vue";
    import Formmultiple from "@/components/Formmultiple.vue";
    import ChallengeQuestion from "@/components/ChallengeQuestion.vue";
    import Formunique from "@/components/Formunique.vue";
    import Liaison from "@/components/Liaison.vue";
    import Ordre from "@/components/Ordre.vue";
    import Classement from "@/components/Classement.vue";
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
    Formmultiple,
    ChallengeQuestion,
    Formunique,
    Liaison,
    Ordre,
    Classement
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
          <div v-if="question.theme =='Théorie'">
            <span className="theorie">*</span>
          </div>
          <Formmultiple :thequestion="question" v-if="question && question.qtype =='form-multiple'" />
          <ChallengeQuestion :thequestion="question" v-if="question && question.qtype =='challenge'" />
          <Formunique :thequestion="question" v-if="question && question.qtype =='form-unique'"/>
          <Liaison :thequestion="question" v-if="question && question.qtype =='liaison'"/>
          <Ordre :thequestion="question" v-if="question && question.qtype =='ordre'" />
          <Classement :thequestion="question" v-if="question && question.qtype =='classement'" />
          </div>
        </div>
    </template>
    
    