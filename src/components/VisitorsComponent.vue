<!-- components/Animals.vue -->
<template>
    <div>
      <h2>Visitors</h2>
      <!-- Display and edit animal data here -->
    </div>
</template>

<script>
export default {
name: 'VisitorsComponent',
props: {
            visitors: {
                type: Array,
                required:true
            }
        },
}
</script>

<style scoped>
/* Component-specific styles */
</style>
  