<script>
    export default {
      name: "App",
      data() {
        return {
          rolledValue: 1,
        };
      },
      methods: {
        roll() {
          this.rolledValue = Math.ceil(Math.random() * 5 + 1);
        },
      },
    };
    </script>
    
    <template>
      <div>
        <button @click="roll">Faire rouler le dice</button>
        <p>rolled dice value: {{ rolledValue }}</p>
      </div>
    </template>