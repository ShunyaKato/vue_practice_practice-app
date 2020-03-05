<template>
  <div class="checklist">
    <h1>研修</h1>
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
      title:
        "職員に対する感染症の研修を、年一回以上、学校内で実施（または施設外の研修へ派遣）している",
      isChecked: false
    },
    {
      title: "派遣研修の場合、研修の内容を職員会議等で共有している",
      isChecked: false
    },
    {
      title:
        "おう吐物処理の方法を教職員の間で確認している（特に冬季胃腸炎流行シーズン頃）",
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