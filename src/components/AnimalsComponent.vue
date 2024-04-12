<template>
    <div>
      <h2>Animals</h2>
    </div>
    <div>
        <!-- <table>
            <tr>
            <td>Name: <br> {{ animal.Species }}</td>
            <td>Nickname: <br> {{ animal.Name }}</td>
            <td>Gender: <br> {{ animal.Gender }}</td>
            <td>Age: <br> {{ animal.Age }}</td>
        </tr>
      </table> -->
    </div>
    <div>
        <button @click="printData">Print</button>
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
            console.log(this.animals.value[0].Name)
        }
    }
}
</script>

<style scoped>
/* Component-specific styles */
</style>