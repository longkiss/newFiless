<template>
  <div class="switch">
    <div class="box" style="margin-bottom: 10px;">
      <zx-switch v-model='values' @change="changevalue(values)" active-text="开" inactive-text="关"></zx-switch>
    </div>
    <div class="box">
      <zx-switch v-model='value' @change="changevalue(value)" active-color="#019dfa" inactive-color="#a3b5bf"></zx-switch>
    </div>
    <div class="box">
      <zx-switch v-model='value1' @change="changevalue(value1)" active-color="#019dfa" inactive-color="#a3b5bf" active-text="开"
        inactive-text="关"></zx-switch>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        values: true,
        value: false,
        value1: false
      };
    },
    methods: {
      changevalue(values) {
        console.log(values);
      }
    },
    created() {
    }
  };
</script>
<style scoped lang="scss">
  .switch {
    padding: 1rem;
  }

  .switch-wrap {
    height: 30px;
    border: 1px solid #ccc;
    border-radius: 30px;
    display: inline-block;
    min-width: 65px;
    position: relative;
    background: #ccc;
    transition: all ease 0.5s;
  }

  .switch-wrap span {
    height: 30px;
    width: 30px;
    display: inline-block;
    border-radius: 30px;
    background: white;
    box-shadow: 0 0 5px #ccc;
    position: absolute;
    top: 0;
    bottom: 0;
    transition: all ease 0.5s;
  }

  .switch-wrap.uncheck {
    background: white;
  }

  .switch-wrap.uncheck span {
    left: 0;
  }

  .switch-wrap.ischeck {
    background: #20a0ff;
    border: 1px solid #20a0ff;
  }

  .switch-wrap.ischeck span {
    left: calc(100% - 30px);
  }
</style>