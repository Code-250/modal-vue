/* eslint-disable key-spacing */
<template>
  <h1>{{title}}</h1>
  <Modal/>
</template>

<script>
import Modal from './components/Modal.vue';

export default {
  components: {
    Modal,
  },
  data() {
    return {
      title: ' My first Vue App :) ',
    };
  },
  methods: {
    handleClick() {
      this.$refs.name.classList.add('active');
      this.$refs.name.focus();
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
