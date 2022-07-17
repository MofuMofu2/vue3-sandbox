<template>
  <div id="counter">
    <p>Click Count {{count}}</p>
    <div>
      <button @click="countUp">Click</button>
      <button class="reset-button" @click="resetCount">Reset</button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {count: 0}
  },
  created() {
    console.info('created', this.$el, this.$data);
  },
  beforeMount() {
    console.info('beforeMount', this.$el, this.$data)
  },
  mounted() {
    console.info('mounted', this.$el, this.$data);
  },
  beforeUpdate() {
    console.info('beforeUpdate', this.$el, this.$data)
  },
  updated() {
    console.info('update', this.$el, this.$data)
  },

  methods: {
    countUp() {
      return this.count = this.count + 1;
    },
    resetCount() {
      return this.count = 0;
    }
  }
}
</script>
<style scoped>
.reset-button {
  margin-left: 1rem;
}
</style>