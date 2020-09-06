<template>
  <div id="app" class="small-container">
    <employee-table :employees="employees"/>
  </div>
</template>

<script>
  import EmployeeTable from '@/components/EmployeeTable.vue'
  import employees from '../tyontekijat.json'

  export default {
    name: 'app',
    components: {
      EmployeeTable,
    },
    data() {
      return {
        employees: employees.employees,
      }
    },
  }

</script>

<style>
  button {
    background: #009435;
    border: 1px solid #009435;
  }

  .small-container {
    max-width: 680px;
  }
</style>