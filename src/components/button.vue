<template>
  <div class="button">
    <zx-button type='primary'>primary</zx-button>
    <zx-button type='success'>success</zx-button>
    <zx-button type='info'>info</zx-button>
    <zx-button type='warning'>warning</zx-button>
    <zx-button type='danger'>danger</zx-button>
    <zx-button type='primary' size='min'>button min</zx-button>
    <zx-button type='primary' size='large'>{{largeButton}}</zx-button>
    <zx-button type='primary' @click="clickFn">click button</zx-button>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        largeButton: 'large button'
      };
    },
    methods: {
      clickFn() {
        this.largeButton = 'this is large button';
      }
    }
  };
</script>
<style scoped>
  .button {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .zx-button {
    margin-bottom: 10px;
  }
</style>