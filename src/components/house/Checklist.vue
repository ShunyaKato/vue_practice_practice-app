<template>
  <div class="checklist">
    <h1>{{ checklists.title }}</h1>
    <ul>
      <li v-for="(list, index) in checklists.lists" :key="index">
        <div v-if="list.title">
          <h2>{{list.title}}</h2>
          <ul>
            <li v-for="(item, index) in list.items" :key="index">
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
export default class Checklist extends Vue {
  @Prop({ type: Object, required: true })
  checklists: any;
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