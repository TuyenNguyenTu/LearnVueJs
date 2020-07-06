<template>
  <div>
    <button @click="showForm()">{{ nameButton }}</button>
    <br />
    <div v-if="isShowFormAdd">
      <b-form-group id="input-group-1" label="Mã Module" label-for="input-1">
        <b-form-input
          id="input-1"
          v-model="form.id"
          type="email"
          required
          placeholder="Enter email"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Tên Module:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          required
          placeholder="Enter name"
        ></b-form-input>
      </b-form-group>

      <b-button @click="handleClickSubmit" variant="primary">Submit</b-button>
      || <b-button @click="resetValue" variant="danger">Reset</b-button> ||
      <b-button @click="hideFormAdd" variant="success">Cancle</b-button>
    </div>
  </div>
</template>
<script>
export default {
  name: "add-module-component",
  data: function() {
    return {
      isShowFormAdd: false,
      nameButton: "Show Form Add Module",
      form: {
        id: "",
        name: "",
      },
      message: "Component children",
    };
  },
  methods: {
    showForm() {
      this.isShowFormAdd = !this.isShowFormAdd;
      if (this.isShowFormAdd) {
        this.nameButton = "Hide Form Add Module";
      } else if (this.isShowFormAdd == false) {
        this.nameButton = "Show Form Add Module";
      }
    },
    hideFormAdd() {
      this.isShowFormAdd = false;
    },
    handleClickSubmit() {
      this.$emit("clicked-send-data", this.form.id, this.form.name);
      alert("Thêm thành công");
      this.resetValue();
    },
    resetValue() {
      document.getElementById("input-2").value = "";
      document.getElementById("input-1").value = "";
    },
  },
  computed: {},
};
</script>
