<template>
  <div class="demo-format">
    <h1>Format Tiền:</h1>
    <h1>{{ tongTien | formatMoney }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tongTien: 1000000,
    };
  },
  filters: {
    formatMoney: function (monney) {
      return monney.toFixed(2).replace(/\d(?=(\d{3})+\.)/g, "$&,");
    },
  },
};
</script>

<style scoped>
.demo-format {
  border: 5px solid #ebebeb;
  padding: 5px 15px;
  margin-right: 10px;
  border-radius: 15px;
}
</style>
