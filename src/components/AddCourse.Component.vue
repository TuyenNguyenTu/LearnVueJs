<template>
  <div>
    <!-- <button @click="showForm">{{ nameButton }}</button> -->
    <b-form inline v-if="isShowFormAddCourse">
      <label class="mr-sm-2" for="inline-form-custom-select-pref">
        Loại danh mục</label
      >

      <select class="mb-2 mr-sm-2 mb-sm-0" v-model="dataOption">
        <option disabled value="">Vui lòng chọn các option</option>
        <option
          v-for="item in parentData"
          :value="item.name"
          v-bind:key="item.id"
          >{{ item.name }}</option
        >
      </select>
      <b-form-input
        v-model="valueInput"
        placeholder="Enter your name"
      ></b-form-input>
      <b-button variant="primary" @click="handleSubmit()">Save</b-button>
    </b-form>
  </div>
</template>
<script>
export default {
  name: "add-course",
  data: function() {
    return {
      isShowFormAddCourse: false,
      nameButton: "Show Form Add Course",
      valueInput: "",
      dataOption: "",
    };
  },
  methods: {
    showForm() {
      this.isShowFormAddCourse = !this.isShowFormAddCourse;
      if (this.isShowFormAddCourse) {
        this.nameButton = "Hide Form Add Course";
      } else if (this.isShowFormAddCourse == false) {
        this.nameButton = "Show Form Add Course";
      }
    },
    handleSubmit() {
      this.$emit("handleToParent", this.valueInput, this.dataOption);
    },
  },
  props: {
    parentData: Array,
  },
};
</script>
