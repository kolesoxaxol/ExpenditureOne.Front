<template>
  <h2>HTML Forms</h2>

  <form>
    <label for="fname">Category name:</label><br />
    <input type="text" id="fname" name="fname" value="John" /><br />
    <label for="lname">Category description</label><br />
    <input type="text" id="lname" name="lname" value="Doe" /><br /><br />
    <input type="button" value="Submit" @click="formSubmitHandler" />
  </form>
</template>

<script>
import axios from "axios";
export default {
  name: "CategoryForm",
  props: {},
  methods: {
    formSubmitHandler: function () {
  
      const data = {
        categoryName: "test",
        color: "black",
      };

      axios
        .post(`https://localhost:44352/api/category`, data, {
          headers: {
            "Content-Type": "application/json",
          },
        })
        .then((response) => {
          console.log("category added");
        })
        .catch((error) => {
          console.log( error);
        })
        .finally(() => {});
    },
    data() {
      return {};
    },
  },
};
</script>
