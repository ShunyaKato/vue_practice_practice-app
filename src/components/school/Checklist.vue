<template>
  <div class="checklist">
    <h1>{{checklists.title}}</h1>
    <ul>
      <li v-for="(list, index) in checklists.lists" :key="index">
        <div v-if="list.title">
          <h2>{{list.title}}</h2>
          <ul>
            <li v-for="(item, index) in list" :key="index">
              <label>
                <input type="checkbox" v-model="item.isChecked" />
                <p>{{ item.item }}</p>
              </label>
            </li>
          </ul>
        </div>
        <label v-else>
          <input type="checkbox" v-model="list.isChecked" />
          <p>{{ list.item }}</p>
        </label>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Checklist1 extends Vue {
  @Prop({ type: Object, required: true })
  checklists: any;
  // items = [
  //   {
  //     title: "園児・児童・生徒が接種した予防接種について確認を行っている",
  //     isChecked: false
  //   },
  //   {
  //     title: "園児・児童・生徒の健康診断の結果を記録している",
  //     isChecked: false
  //   },
  //   {
  //     title: "園児・児童・生徒の毎日の健康観察を実施している",
  //     isChecked: false
  //   },
  //   {
  //     title:
  //       "園・学校全体の体調不良者・欠席者等の情報（人数や欠席理由等）が１日１回集約されている",
  //     isChecked: false
  //   },
  //   {
  //     title:
  //       "園児・児童・生徒の体調が悪い場合には、本人・保護者に受診を促している",
  //     isChecked: false
  //   }
  // ];
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