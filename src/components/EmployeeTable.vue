<template>
    <div id="employee-table">
        <table>
            <thead>
            <tr>
                <th>First name</th>
                <th>Last name</th>
                <th>Address</th>
                <th>Phone (home)</th>
                <th>Phone (work)</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="employee in employees" :key="employee.id">
                <td>{{ employee.firstName }}</td>
                <td>{{ employee.lastName }}</td>
                <td>{{ employee.address }}</td>
                <td> {{ employee.phone != null ? employee.phone[0].home: "" }}</td>
                <td> {{ employee.phone != null ? employee.phone[0].work: "" }}</td>
            </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
  export default {
    name: 'employee-table',
    props: {
      employees: Array,
    }
  };


</script>

<style scoped>

</style>