<template>
  <div class="hello">
    <div class="img-container">
      <img src="@/assets/分数背景@2x.png" alt />
      <div class="description2">
        <Description2 score="100" />
      </div>
      
      <Description1 class="description1" name="和同学" percent="80%" />
      <AnswerList></AnswerList>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import Description1 from "@/components/Description1.vue";
import Description2 from "@/components/Description2.vue";
import AnswerList from "@/components/AnswerList.vue";

@Component({
  components: { Description1, Description2, AnswerList }
})
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.img-container {
  position: relative;

  img {
    width: 100%;
  }

  .description1 {
    position: absolute;
    top: .5rem;
    right: 0;
  }

  .description2 {
    position: absolute;
    top: 0;
    left: 0;
  }
}
</style>
