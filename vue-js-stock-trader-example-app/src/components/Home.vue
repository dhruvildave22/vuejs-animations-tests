<template>
  <div>
    <h1>Trade or View your Portfolio</h1>
    <h6>You may save & load you data</h6>
    <h6>Click on End Day to begin a new Day!</h6>
    <hr />
    <p>Your Funds: ${{ formatPrice(funds) }}</p>
  </div>
</template>
<script>
export default {
  computed: {
    funds() {
      return this.$store.getters.funds;
    }
  },
  methods: {
    formatPrice(value) {
      let val = (value / 1).toFixed(2).replace(",", ".");
      return val.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    }
  }
};
</script>