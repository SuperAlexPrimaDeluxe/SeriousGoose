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
        <div class="superdice" @click="roll"><span>{{ rolledValue }}</span></div>
      </div>
    </template>