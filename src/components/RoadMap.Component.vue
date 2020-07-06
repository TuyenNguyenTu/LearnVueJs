<template>
  <div>
    <ModuleComponent
      v-for="item in listModule"
      v-bind:key="item.id"
      :name="item.name"
    ></ModuleComponent>
  </div>
</template>
<script>
import ModuleComponent from "./Module.Component";
export default {
  name: "road-map-component",
  components: {
    ModuleComponent,
  },
  data: function() {
    return {
      listModule: [
        {
          id: 1,
          name: "C#",
        },
        {
          id: 2,
          name: "Entity Framework",
        },

        {
          id: 3,
          name: "ASP .NET Basic",
        },
        {
          id: 4,
          name: "C#",
        },
        {
          id: 5,
          name: "SQL Fundamentals",
        },
      ],
    };
  },
};
</script>
