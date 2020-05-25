<template>
  <div class="hello">
    <span class="name">{{name}}</span>超过了全国
    <span class="percent">{{percent}}</span>的同 龄孩子，数感运算、观察能力突出
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Description1 extends Vue {
  @Prop() private name!: string;
  @Prop() private percent!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.hello {
    width: 4.18rem;
    font-size: .28rem;
    span {
        color: #FFEB0C;
    }
}
</style>
