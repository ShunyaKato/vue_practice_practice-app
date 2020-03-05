<template>
  <div class="checklist">
    <h1>教職員の健康管理と早期発見</h1>
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
export default class Checklist2 extends Vue {
  items = [
    {
      title: "教職員の健康診断を定期的に実施し、未受診者に受診を促している",
      isChecked: false
    },
    {
      title: "教職員の体調が悪い場合には、医療機関へ受診させている",
      isChecked: false
    },
    {
      title:
        "学校内に出入りするパート職員やボランティア等の健康状態を確認している",
      isChecked: false
    },
    {
      title: "実習生の予防接種歴・健康診断の結果を必要に応じて提出させている",
      isChecked: false
    },
    {
      title:
        "実習生の毎日の健康状態を確認している（発熱・咳・おう吐・下痢等の有無）",
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