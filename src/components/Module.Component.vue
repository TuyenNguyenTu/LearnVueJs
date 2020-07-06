<template>
  <div>
    <b-col style="text-align:center; border:1px solid black">
      <h1>{{ name }}</h1>
      <b-row>
        <CourseComponent
          v-for="item in listCourse"
          v-bind:key="item.id"
          :title="item.name"
        ></CourseComponent>
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
    parentData: String,
  },
  components: {
    CourseComponent,
  },
  data: function() {
    return {
      listCourse: [
        {
          id: 1,
          name: "Web",
        },
        {
          id: 2,
          name: "Desktop",
        },
        {
          id: 3,
          name: "Mobile",
        },
      ],
    };
  },
};
</script>
