<script >

import axios from "axios";
import Ordre from "@/components/Ordre.vue";
import Liaison from "./Liaison.vue";
import Formmultiple from "./Formmultiple.vue";
import Formunique from "./Formunique.vue";
export default {
  data() {
        return {
          posts: [],
          isActive: false,
          id: null
        };
      },

      components: {
    Ordre,
    Liaison,
    Formmultiple,
    Formunique
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
            this.posts = response.data;

          });
      },
    };
  </script>
  
 


<template>
  <div class="Megacontainer">
<div class="de" v-for="(question, key) in posts" :key="key">
<!-- <Ordre class="static" :class="{ active: isActive }" v-if="question && question.qtype =='ordre'">FKSD</Ordre> -->
<!-- <div class="ordre static" :class="{ active: isActive }" v-if="question && question.qtype =='ordre'">ferjlf</div> -->
<!-- <div  class="static" :class="{ active: isActive, 'text-danger': hasError }"> -->
<!-- <Ordre :thequestion="question" v-if="question && question.qtype =='ordre'"/> -->
<!--</div>-->

<div class="theorie" v-if="question && question.theme =='Théorie'">
  {{ question.number }}
</div>

<div class="domestique" v-else-if="question && question.theme =='Domestique'">
  {{ question.number }}
</div>

<div class="economique" v-else-if="question && question.theme =='Économique'">
  {{ question.number }}
</div>

<div class="pulique-politique" v-else-if="question && question.theme =='Publique / politique'">
  {{ question.number }}
</div>


</div>
</div>


<Formmultiple></Formmultiple>
<Formunique></Formunique> 
<Ordre></Ordre>
<Liaison></Liaison> 

<!-- <Formmultiple :thequestion="question"></Formmultiple> -->
  </template>