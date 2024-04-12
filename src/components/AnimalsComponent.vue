<template>
    <div>
      <h2>Animals</h2>
    </div>
    <div>
        <table v-for="object in this.animals.value">
            
            <tr>Species: {{ object.Species }}</tr>
           <tr>Name: {{ object.Name }}</tr>
           <tr>Age: {{ object.Age }}</tr>
           <tr>Gender: {{ object.Gender }}</tr>

        </table>
    </div>
    <div>
        <button @click="printData">Print</button>
    </div>
</template>

<script>
import { dotmap } from 'dot-prop-immutable'
export default {
    name: 'AnimalsComponent',
    props: {
        animals: {
            type: Object,
            required:true
        }
    },
    methods: {
        printData() {
            console.log(this.animals.value[0].Name)
        },
        getAnimalProp(animal, proerty){
            return dotmap.get(animal, proerty)
        },
    }
}
</script>

<style scoped>
/* Component-specific styles */
</style>