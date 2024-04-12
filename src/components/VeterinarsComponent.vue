<!-- components/Animals.vue -->
<template>
    <div>
      <h2>Veterinars</h2>
      <!-- Display and edit animal data here -->
    </div>
</template>

<script>
export default {
name: 'VeterinarsComponent',
props: {
            veterinars: {
                type: Array,
                required:true
            }
        },
}
</script>

<style scoped>
/* Component-specific styles */
</style>
  