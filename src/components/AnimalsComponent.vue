<template>
    <div>
      <h2>Animals</h2>
    </div>
    <div>
        <table v-for="animal in this.animals" :key="animal.id">
        <tr>
            <td>Name: <br> {{ animal.species }}</td>
            <td>Nickname: <br> {{ animal.name }}</td>
            <td>Gender: <br> {{ animal.gender }}</td>
            <td>Age: <br> {{ animal.age }}</td>
        </tr>
      </table>
    </div>
</template>

<script>
export default {
    name: 'AnimalsComponent',
    props: {
        animals: {
            type: Array,
            required:true
        }
    },
    methods: {
        printData() {
            console.table(this.animals)
        }
    }
}
</script>

<style scoped>
/* Component-specific styles */
</style>