<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <CategoryForm />
  
</template>

<script>
import CategoryForm from './components/category/CategoryForm.vue'
import Chart from './components/TestChart.vue'

export default {
  name: 'App',
  components: {
    CategoryForm,
    Chart
  }
}
</script>
