<template>
  <div class="checklist">
    <h1>手洗いと標準予防策</h1>
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
export default class Checklist3 extends Vue {
  items = [
    {
      title: "園児・児童・生徒へ手洗いの指導を行っている",
      isChecked: false
    },
    {
      title: "手洗いは、石鹸と流水で、15秒～30秒以上行っている",
      isChecked: false
    },
    {
      title:
        "手拭きは使い捨てのペーパータオルか個人用のタオルを使用している(共用タオルは置いていない）",
      isChecked: false
    },
    {
      title: "来訪者に手洗いを勧めている",
      isChecked: false
    },
    {
      title: "使い捨て手袋を使用した場合、手袋をはずした後に手洗いをしている",
      isChecked: false
    },
    {
      title:
        "園児・児童・生徒・教職員に咳症状がある場合、周囲への飛散を防ぐためマスクの着用を促している",
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