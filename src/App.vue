<script setup>
  import AnimalsComponent from './components/AnimalsComponent.vue'
  import EnclosuresComponent from './components/EnclosuresComponent.vue'
  import FeedingsComponent from './components/FeedingsComponent.vue'
  import MedicalRecordsComponent from './components/MedicalRecordsComponent.vue'
  import VeterinarsComponent from './components/VeterinarsComponent.vue'
  import VisitorsComponent from './components/VisitorsComponent.vue'
  import ZookeepersComponent from './components/ZookeepersComponent.vue'
  import items from './data/idea.js'

  import { defineProps } from 'vue'
  // console.log(items.items)
  defineProps({
    animals: {
      type: Array,
      required: true
    },
    enclosures: {
      type: Array,
      required: true
    },
    zookeepers: {
      type: Array,
      required: true
    },
    visitors: {
      type: Array,
      required: true
    },
    feedings: {
      type: Array,
      required: true
    },
    medical_records: {
      type: Array,
      required: true
    },
    veterinars: {
      type: Array,
      required: true
    }
  })

</script>

<!-- <script>

  export default {
  "item": {
    "animals": items.animals,
    "enclosures": items.enclosures,
    "zookeepers": items.zookeepers,
    "visitors": items.visitors,
    "feedings": items.feedings,
    "medical_records": items.medical_records,
    "veterinars": items.veterinars

  }
} -->
<!-- 
</script> -->

<template>
  <div>
    <AnimalsComponent :animals="items.items.animals" />
    <EnclosuresComponent :enclosures="items.items.enclosures" />
    <FeedingsComponent :feedings="items.items.feedings" />
    <MedicalRecordsComponent :medical_records="items.items.medical_records" />
    <VeterinarsComponent :veterinars="items.items.veterinars" />
    <VisitorsComponent :visitors="items.items.visitors" />
    <ZookeepersComponent :zookepers="items.items.zookeepers" />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
