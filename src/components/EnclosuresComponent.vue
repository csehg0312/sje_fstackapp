<!-- components/Animals.vue -->
<template>
    <div>
      <h2>Enclosures</h2>
      <table>
        <tr>
            <td>Enclosure name: </td>
            <td>Size: </td>
            <td>Habitat: </td>
        </tr>
        <!-- <div v-for="enclosure in this.enclosures" :key="enclosure.enclosure_id">
            <tr>
                <td>{{ enclosure.enclosure_name }}</td>
                <td>{{ enclosure.size }}</td>
                <td>{{ enclosure.habitat_type }}</td>
            </tr>
        </div> -->
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
  