/* eslint-disable key-spacing */
<template>
  <h1>{{title}}</h1>
  <p>Welcome....</p>
  <div v-if="showModal">
  <Modal theme="saled" @close="toggleModal">
    <template v-slot:links>
      <a href="#">signup</a>
      <a href="#">get more info</a>
    </template>
    <h1>Becoming a Ninja</h1>
    <p>there is a way that any one can become a ninja</p>
  </Modal>
  </div>
  <teleport to=".modals" v-if="showModal2">
    <Modal @close="toggleModal2">
     <h1>hello world</h1>
     <p>please make it work</p>
    </Modal>
  </teleport>
  <button @click="toggleModal">open modal</button>
  <button @click="toggleModal2">open modal 2</button>
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
      header: 'sign up for some videos',
      text: 'there are more you can see',
      showModal: false,
      showModal2: false,
    };
  },
  methods: {
    handleClick() {
      this.$refs.name.classList.add('active');
      this.$refs.name.focus();
    },
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModal2() {
      this.showModal2 = !this.showModal2;
    },
  },
};
</script>

<style>
#app, .modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
