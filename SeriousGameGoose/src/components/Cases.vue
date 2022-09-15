<script >

import axios from "axios";
import Ordre from "@/components/Ordre.vue";
export default {
  data() {
        return {
          posts: [],
          isActive: false,
        };
      },

      components: {
        Ordre
      },
  methods: {
    toggleComponentOne () {
      alert("fdp");
      this.isActive = !this.isActive;
      console.log(this.isActive);
    },
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



<div class="de" v-for="(question, key) in posts" :key="key"  @click="toggleComponentOne">


<div class="ordre" v-if="question && question.qtype =='ordre'" ></div>
  <Ordre :class="{ active: isActive, 'text-danger': hasError }" :thequestion="question" v-if="question && question.qtype =='ordre'"/>

<div class="theorie" v-if="question && question.theme =='Théorie'">
  {{ question.number }}
</div>

<div class="domestique" v-else-if="question && question.theme =='Domestique'">
  {{ question.number }}
</div>
    <!--<div class="lol" @click="toggleComponentOne"></div>-->
 
  </div>
  </template>