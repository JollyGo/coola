<template>
  <el-card class="numberCard" shadow="hover">
    <!-- <i v-bind:class='[icon, iconWarp]'></i> -->
    <d2-icon name="users" class="iconWarp" :style="{color:color}" />
    <div class="content">
      <p class="title">{{title}}</p>
      <p class="number iCountUp">
        <ICountUp :delay="delay" :endVal="endVal" :options="options" @ready="onReady" />
      </p>
    </div>
  </el-card>
</template>

<script>
import ICountUp from "vue-countup-v2";
export default {
  components: {
    ICountUp
  },
  props: {
    icon: { type: String, required: true },
    color: { type: String, default: "orange" },
    title: { type: String, required: true }
  },
  data() {
    return {
      delay: 100,
      endVal: 120500,
      options: {
        useEasing: true,
        useGrouping: true,
        separator: ",",
        decimal: ".",
        prefix: "",
        suffix: ""
      }
    };
  },
  methods: {
    onReady: function(instance, CountUp) {
      const that = this;
      instance.update(that.endVal + 100);
    }
  }
};
</script>

<style lang='scss' scoped>
.numberCard {
  padding: 32px;
  margin-bottom: 24px;
  cursor: pointer;
  .iconWarp {
    font-size: 54px;
    float: left;
  }
  .content {
    widows: 100%;
    padding-left: 78px;
    .title {
      line-height: 16px;
      font-size: 16px;
      margin-bottom: 8px;
      height: 16px;
      text-overflow: ellipsis;
    }
    .number {
      line-height: 32px;
      font-size: 24px;
      height: 32px;
      text-overflow: ellipsis;
      margin-bottom: 0;
    }
  }
}
.iCountUp {
  font-size: 1em;
  margin: 0;
  color: #4d63bc;
}
</style>