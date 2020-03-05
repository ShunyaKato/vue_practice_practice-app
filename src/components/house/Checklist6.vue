<template>
  <div class="checklist">
    <h1>掃除</h1>
    <h2>トイレ</h2>
    <ul>
      <li v-for="(toilet, index) in toilets" :key="index">
        <label>
          <input type="checkbox" v-model="toilet.isChecked" />
          <p>{{ toilet.title }}</p>
        </label>
      </li>
    </ul>
    <h2>お風呂</h2>
    <ul>
      <li v-for="(bath, index) in bathes" :key="index">
        <label>
          <input type="checkbox" v-model="bath.isChecked" />
          <p>{{ bath.title }}</p>
        </label>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Checklist6 extends Vue {
  toilets = [
    {
      title: "専用の手袋を用いている",
      isChecked: false
    },
    {
      title: "日ごろからこまめに掃除をしている",
      isChecked: false
    },
    {
      title:
        "消毒する場合は、汚れをあらかじめ落としてから、消毒液を含ませた布等で拭いている（噴霧の場合、消毒液がすぐ乾燥しないように十分な量を噴霧し、拭き取っている）",
      isChecked: false
    },
    {
      title: " 清掃後、手袋を外した後も手洗いをしている",
      isChecked: false
    }
  ];
  bathes = [
    { title: "浴槽は流水と石鹸で十分洗い流している", isChecked: false },
    {
      title: "浴槽の他、風呂の床、洗面器、椅子なども掃除している",
      isChecked: false
    }
  ];
}
</script>

<style lang="scss">
.checklist {
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
    width: 700px;
    margin: 0 auto;
    li {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      text-align: left;
      label {
        display: flex;
        p {
          margin: 0;
        }
      }
    }
  }
}
</style>