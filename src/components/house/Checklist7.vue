<template>
  <div class="checklist">
    <h1>感染症予防のための環境整備</h1>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        <label>
          <input type="checkbox" v-model="item.isChecked" />
          <p>{{ item.title }}</p>
        </label>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Checklist5 extends Vue {
  items = [
    {
      title: "洗面所、トイレに石鹸を置いている",
      isChecked: false
    },
    {
      title:
        "階段の手すり、水道の蛇口等頻繁に触れる場所を定期的に清掃（消毒）している",
      isChecked: false
    },
    {
      title: "おう吐物等を処理するための物品を準備している",
      isChecked: false
    },
    {
      title: " 訪問者に手洗いを勧めている",
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