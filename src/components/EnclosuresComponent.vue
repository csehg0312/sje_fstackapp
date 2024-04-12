<!-- components/Animals.vue -->
<template>
    <div>
      <h2>Enclosures</h2>
      <table v-for="object in this.enclosures.value">
            
            <tr>Species: {{ object.Species }}</tr>
           <tr>Name: {{ object.Name }}</tr>
           <tr>Age: {{ object.Age }}</tr>
           <tr>Gender: {{ object.Gender }}</tr>

        </table>
    </div>
</template>

<script>
export default {
    name: 'EnclosuresComponent',
    props: {
            enclosures: {
                type: Array,
                required:true
            }
        },
    
}
</script>

<style scoped>
/* Component-specific styles */
</style>
  