<template>
  <h1>Categories:</h1>
 <div v-for="category in this.categoryListItems" :key="category.id">
    {{ category.categoryName }}
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "CategoryList",
  props: {},
  data() {
    return {
     categoryListItems:[], 
     datas: ''
    };
  },
  methods: {},
  mounted()  {
    axios
      .get(`https://localhost:44352/api/category`, {
        headers: {
          "Content-Type": "application/json",
        },
      })
      .then((response) => {
        console.debug("Category list: getCategories List");
        console.debug(response.data.data);
        this.categoryListItems = response.data.data;
      })
      .catch((error) => {
        console.log(error);
      })
      .finally(() => {});
  },
  data() {
    return {};
  },
};
</script>
