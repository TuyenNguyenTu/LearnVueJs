<template>
  <div>
    <b-card :title="handleText" style="max-width: 20rem;" class="mb-2">
      <b-card-text>
        {{ description }}
      </b-card-text>
    </b-card>
  </div>
</template>
<script>
export default {
  name: "level-component",
  props: {
    title: String,
    description: String,
  },
  computed: {
    handleText() {
      return this.title;
    },
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
