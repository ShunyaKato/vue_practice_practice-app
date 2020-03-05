<template>
  <div class="checklist">
    <h1>食事に関する対策</h1>
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
      title: "調理前の手洗いは洗面台でしている",
      isChecked: false
    },
    {
      title: "高齢者や乳幼児へは、貝類の生食を避けている",
      isChecked: false
    },
    {
      title: "加熱できるものは中までしっかり加熱している",
      isChecked: false
    },
    {
      title: "作った食事はできるだけ早く食べている",
      isChecked: false
    },
    {
      title: "食器、調理器具は熱湯又は消毒液で消毒後、水洗いして乾燥させている",
      isChecked: false
    },
    {
      title: "冷蔵庫の中を掃除している",
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