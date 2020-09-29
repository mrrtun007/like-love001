<template>
  <div>
    <button v-on:click="upFunction" class="btn btn-dark">ถูกใจมาก</button>
    <button v-on:click="downFunction" class="btn btn-dark ml-3">ไม่ถูกใจอย่างแรง</button>
    <button v-on:click="LoveFunction" class="btn btn-dark ml-3">รักมากมาย</button>
    <button v-on:click="ResetFunction" class="btn btn-dark ml-3">รีเซ็ท</button>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
  props: {
    lable: String,
  },
  methods: {
    upFunction: function () {
      this.counter += 1;
      this.$emit("cc", this.counter);
    },

    downFunction: function () {
      this.counter += -5;
      this.$emit("cc", this.counter);
    },

    LoveFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
  },
};
</script>
<style>
</style>