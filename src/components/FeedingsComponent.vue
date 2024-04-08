<!-- components/Animals.vue -->
<template>
    <div>
      <h2>Feedings</h2>
      <!-- Display and edit animal data here -->
    </div>
</template>

<script>
export default {
name: 'FeedingsComponent',
    props: {
            feedings: {
                type: Array,
                required:true
            }
        },
    }
</script>

<style scoped>
/* Component-specific styles */
</style>
  