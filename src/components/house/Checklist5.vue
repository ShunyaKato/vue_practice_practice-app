<template>
  <div class="checklist">
    <h1>入浴時の対策</h1>
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
      title: "浴槽に入る前に、お尻をよく洗っている",
      isChecked: false
    },
    {
      title: "風呂の水は毎日かえている",
      isChecked: false
    },
    {
      title: "タオルやバスタオルは共用していない",
      isChecked: false
    },
    {
      title: " 下痢をしている患者の入浴は一番最後にしている",
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