<template>
  <div>
    <div>Cool Beans, let's start the input</div>
    <input @input="handleChange" :placeholder="placeholder" />
    <div>Value: {{ value }}</div>
    <button @click="increment">Increment Top Count</button>
  </div>
</template>

<script>
export default {
  props: {
    placeholder: String,
    topCount: Number,
  },
  data() {
    return {
      value: "",
      count: this.topCount,
    };
  },
  methods: {
    handleChange(e) {
      this.value = e.target.value;
    },
    increment() {
      this.$emit("topcountup");
    },
  },
};
</script>