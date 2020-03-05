<template>
  <div class="checklist">
    <h1>手洗い</h1>
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
      title:
        "帰宅後、調理前、配膳前、食事前、排泄後、排泄のお世話後には手洗いを実施している",
      isChecked: false
    },
    {
      title: "爪は短く切り、時計や指輪を外している",
      isChecked: false
    },
    {
      title: "石鹸を使い、流水で 15～30 秒以上こすり洗いをしている",
      isChecked: false
    },
    {
      title:
        "汚れが残りやすい、指先や爪の間、指の間、親指の周り、手首、手のしわも注意して洗っている",
      isChecked: false
    },
    {
      title:
        "手洗い後の手拭用タオルは共用せず、ペーパータオルや個人用タオルを利用している",
      isChecked: false
    },
    {
      title:
        "水道の蛇口は手と一緒に洗うか、ペーパータオルを利用して、蛇口を締めている",
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