<template>
  <div class="hello">
      <span class="score">{{score}}</span>
      <span class="label">测评成绩</span>
      <img src="@/assets/成绩@2x.png" alt />
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Description2 extends Vue {
  @Prop() private score!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.hello {
    position: relative;

    .score {
        position: absolute;
        color: #DE6A38;
        font-size: .52rem;
        top: .38rem;
        left: .58rem;
    }

    .label {
        position: absolute;
        color: #FFFFFF;
        font-size: .24rem;
        bottom: .47rem;
        left: .55rem;
    }

    img {
        width: 2.1rem;
    }
}
</style>
