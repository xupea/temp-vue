<template>
  <div class="container">
    <img class="item" v-for="(item, index) in answerList" :src="item.src" :key="index" />
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

interface Answer {
  correct: boolean;
}

@Component
export default class AnswerList extends Vue {
  @Prop() private list!: Answer[];

  get answerList() {
    return this.list && this.list.map(item => ({
      src: item.correct ? "/assets/对@2x.png" : "/assets/错@2x.png"
    }));
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.container {
  display: flex;
  flex-wrap: wrap;
  width: 4.18rem;
  font-size: 0.28rem;

  img {
    width: .58rem;
    height: .58rem;
  }
}
</style>
