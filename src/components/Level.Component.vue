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
    return {};
  },
};
</script>
