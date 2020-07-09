<template>
  <div id="app">
    <h1 class="animate__animated animate__headShake">{{ titulo }}</h1>

    <div class="form-group">
      <label class="col-form-label">
        Digite o valor de
        <strong>R1</strong>
      </label>
      <input
        @focus="$event.target.select()"
        type="number"
        class="form-control animate__animated animate__wobble"
        name="r1"
        placeholder="R1"
        id="inputDefault"
        v-model="r1"
      />
    </div>

    <div class="form-group">
      <label class="col-form-label">
        Digite o valor de
        <strong>R2</strong>
      </label>
      <input
        @focus="$event.target.select()"
        type="number"
        class="form-control animate__animated animate__jello"
        name="r2"
        placeholder="R2"
        id="inputDefault"
        v-model="r2"
      />
    </div>

    <h2 class="text-primary">{{ result || 0 }}</h2>

    <button class="animate__animated animate__tada btn-warning" @click="zerar">zerar</button>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      titulo: "Resistores do Negão",
      r1: "",
      r2: ""
    };
  },
  computed: {
    result() {
      return (
        (parseFloat(this.r1) * parseFloat(this.r2)) / parseFloat(this.r1) +
        parseFloat(this.r2)
      );
    }
  },
  methods: {
    zerar: function() {        
        this.r1 = 0
        this.r2 = 0
     }
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Cousine:wght@400;700&display=swap");

*,
html,
body {
  box-sizing: border-box;
  width: 100%;
  font-family: "Cousine", monospace;
  text-align: center;
  color: rgba(240, 248, 255, 0.658);
}

button {
  width: 50%;
}

h1 {
  padding: 1rem;
}

h2 {
  padding: 1rem;
  font-weight: bold;
}

.form-group {
  width: 50%;
  margin: 0 auto;
}
</style>
