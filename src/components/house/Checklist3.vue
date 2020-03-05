<template>
  <div class="checklist">
    <h1>排泄に関する対策</h1>
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
      title: "使用前に便座を消毒している",
      isChecked: false
    },
    {
      title: "排便後お尻を拭いた後、何も触らずすぐに手を洗っている",
      isChecked: false
    },
    {
      title: "可能であれば、排便後の手洗いはトイレの中で行っている",
      isChecked: false
    },
    {
      title:
        "ポンプ式石鹸や水道の蛇口、トイレのドアノブ、水洗レバーはペーパータオルを使うなどして、手洗い前に直接触らないようにしている",
      isChecked: false
    },
    {
      title: "蛇口は清潔に保ち、必要に応じて消毒している",
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