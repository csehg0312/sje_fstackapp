<!-- components/Animals.vue -->
<template>
    <div>
      <h2>Zookeepers</h2> 
      <table v-for="zookeeper in this.zookeepers" :key="zookeeper.keeper_id">
        {{ zookeeper.keeper_name }}
        <h1>hey</h1>
      </table>
    </div>
</template>

<script>
export default {
    name: 'ZookeepersComponent',
    props: {
                zookeepers: {
                    type: Array,
                    required:true
                }
            },
    }
</script>

<style scoped>
/* Component-specific styles */
</style>
  