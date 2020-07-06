<template>
  <div>
    <b-col style="text-align:center; border:1px solid black">
      <h1>{{ name }}</h1>
      <b-row>
        <CourseComponent></CourseComponent>
      </b-row>
    </b-col>
  </div>
</template>
<script>
import CourseComponent from "./Course.Component";

export default {
  name: "module-component",
  props: {
    name: String,
  },
  components: {
    CourseComponent,
  },
  data: function() {
    return {};
  },
};
</script>
