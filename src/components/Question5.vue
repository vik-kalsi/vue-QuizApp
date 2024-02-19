<script>
export default {
  emits: ['HideQ5', 'updateScoreQ5'],
  data() {
    return {
      Question: "What is the biggest continent on Earth?",
    };
  },
  methods: {
    Q5Correct() {
        alert("Correct Answer");
        this.$emit("HideQ5");
        this.$emit("updateScoreQ5");
    },
    Q5Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ5");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 5: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q5Wrong"> Africa </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q5Correct"> Asia </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q5Wrong"> North America </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q5Wrong"> Europe </button>
  </div>

</template>