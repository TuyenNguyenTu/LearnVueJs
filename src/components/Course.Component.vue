<template>
  <div>
    <b-container style="padding-left:5px;">
      <h2>{{ title }}</h2>
      <LevelComponent
        v-for="item in listLevel"
        v-bind:key="item.id"
        :title="item.name"
        style="text-align:center;"
        :description="item.desciption"
      ></LevelComponent>
    </b-container>
  </div>
</template>
<script>
import LevelComponent from "./Level.Component";
export default {
  name: "course-basic",
  props: {
    title: String,
  },
  components: {
    LevelComponent,
  },
  data: function() {
    return {
      listLevel: [
        {
          id: 1,
          name: "Learn the basic of Entity Framework",
          desciption: "Document from Microsoft",
        },
        {
          id: 2,
          name: "Code First + Migrations",
          desciption: "Document from Microsoft",
        },
        {
          id: 3,
          name: "Change Tracker API",
          desciption: "Document from Microsoft",
        },
        {
          id: 4,
          name: "Lazy Loading Eager Loadingm, Explicit Loading",
          desciption: "Document from Microsoft",
        },
      ],
    };
  },
};
</script>
