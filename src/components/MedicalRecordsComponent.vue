<!-- components/Animals.vue -->
<template>
    <div>
      <h2>MedicalRecords</h2>
      <!-- Display and edit animal data here -->
    </div>
</template>

<script>
export default {
name: 'MedicalRecordsComponent',
props: {
    medical_records: {
        type: Array,
        required:true
    }
    },
}
</script>

<style scoped>
/* Component-specific styles */
</style>
  