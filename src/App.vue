<template>
  <CategoryForm />

  <CategoryList />
  
</template>

<script>
import CategoryForm from './components/category/CategoryForm.vue';
import CategoryList from './components/category/CategoryList.vue';
import Chart from './components/TestChart.vue';

export default {
  name: 'App',
  components: {
    CategoryForm,
    CategoryList,
    Chart
  }
}
</script>
