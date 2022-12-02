<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" width="600px">
      <template v-slot:activator="{ on, attrs }">
        <v-btn color="primary" dark v-bind="attrs" v-on="on">
          Open Dialog
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">Use Google's location service?</span>
        </v-card-title>
      </v-card>
    </v-dialog>
  </v-row>
</template>
<script>
// this.$emit('add-task')
export default {
  props: {
    title: {
      type: String,
      default: "",
    },
    priority: {
      type: Object,
      default: { label: "Very High", value: "very-high", color: "red" },
    },
    isEdit: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      name: "AddDialog",
      dialog: false,
      optionDropdown: false,
      optons: [
        {
          label: "Very High",
          value: "very-high",
          color: "red",
        },
        {
          label: "High",
          value: "high",
          color: "red",
        },
        {
          label: "Medium",
          value: "normal",
          color: "red",
        },
        {
          label: "Very Low",
          value: "very-low",
          color: "red",
        },
        {
          label: "Low",
          value: "low",
          color: "red",
        },
      ],
    };
  },
  methods: {
    setData() {
      this.priority = props.priority;
      this.title = props.title;
    },
    setOptions(options) {
      this.priority = options;
      this.optionDropdown = false;
    },
    setToogle() {
      this.dialog = !this.dialog;
      return;
    },
  },
};
</script>
