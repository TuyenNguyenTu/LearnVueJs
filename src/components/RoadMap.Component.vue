<template>
  <div>
    <AddModule @clicked-send-data="HandleClickInParent"></AddModule>
    <br />
    <AddCourse :parentData="listModule"></AddCourse>
    <br />
    <ModuleComponent
      v-for="item in listModule"
      v-bind:key="item.id"
      :name="item.name"
    ></ModuleComponent>
  </div>
</template>
<script>
import AddModule from "./AddModule.Component";
import ModuleComponent from "./Module.Component";
import AddCourse from "./AddCourse.Component";
export default {
  name: "road-map-component",
  components: {
    ModuleComponent,
    AddModule,
    AddCourse,
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
      dataFromChildrenComponent: {
        id: "",
        name: "",
      },
    };
  },
  methods: {
    HandleClickInParent(dataChil1, dataChil2) {
      this.dataFromChildrenComponent.id = dataChil1;
      this.dataFromChildrenComponent.name = dataChil2;
      this.listModule.push({
        id: this.dataFromChildrenComponent.id,
        name: this.dataFromChildrenComponent.name,
      });
    },
  },
};
</script>
