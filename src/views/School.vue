<template>
  <div class="School">
    <h1>学校等</h1>
    <Checklist1 />
    <Checklist2 />
    <Checklist3 />
    <Checklist4 />
    <Checklist5 />
  </div>
</template>

<script>
import Checklist1 from "../components/school/Checklist1";
import Checklist2 from "../components/school/Checklist2";
import Checklist3 from "../components/school/Checklist3";
import Checklist4 from "../components/school/Checklist4";
import Checklist5 from "../components/school/Checklist5";

export default {
  name: "school",
  components: {
    Checklist1,
    Checklist2,
    Checklist3,
    Checklist4,
    Checklist5
  }
};
</script>
