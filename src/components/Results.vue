/* eslint-disable no-return-assign */
<template>
  <h2>The reaction time would be..</h2>
  <p>the reaction time is : {{score}} ms</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
  name: 'Results',
  props: ['score'],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 300) {
      this.rank = 'you have got black belt';
    } else if (this.score < 500) {
      this.rank = 'you got yourself blue belt';
    } else {
      this.rank = 'still on white belt';
    }
  },
};
</script>

<style>
.rank{
    font-size:1.4em;
    color:#0faf87;
    font-weight:bold;
}
</style>
