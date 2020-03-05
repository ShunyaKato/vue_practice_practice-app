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
export default class Checklist4 extends Vue {
  items = [
    {
      title: "手洗い場・トイレに石鹸が整備されている",
      isChecked: false
    },
    {
      title:
        "階段の手すり・水道の蛇口等、園児・児童・生徒が頻繁に触れる場所を定期的に清掃（消毒）している",
      isChecked: false
    },
    {
      title:
        "感染症予防・発生時対応のための物品が準備されている（※使い捨て手袋・マスク・エプロン・拭き取りの布（ペーパータオル、新聞紙等）、塩素系消毒剤、ビニール袋、専用バケツなど）",
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