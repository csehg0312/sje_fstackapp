<script setup>
  // import Axios from 'axios'
  import AnimalsComponent from './components/AnimalsComponent.vue'
  import EnclosuresComponent from './components/EnclosuresComponent.vue'
  import FeedingsComponent from './components/FeedingsComponent.vue'
  import MedicalRecordsComponent from './components/MedicalRecordsComponent.vue'
  import VeterinarsComponent from './components/VeterinarsComponent.vue'
  import VisitorsComponent from './components/VisitorsComponent.vue'
  import ZookeepersComponent from './components/ZookeepersComponent.vue'
  import { onMounted, ref } from 'vue'
  import getRoutes from './js/routes'

  const items = { 
    animals: ref([]),
    enclosures: ref([]),
    feedings:ref([]),
    medical_records: ref([]),
    veterinars: ref([]),
    visitors: ref([]),
    zookeepers: ref([])
  }

  // const axiosInstance = Axios.create({
  //   baseURL: 'http://localhost:3001' 
  // })

  const fetchData = async () => {
    const [
        animalsResponse,
        enclosuresResponse,
        feedingsResponse,
        medicalRecordsResponse,
        veterinarsResponse,
        visitorsResponse,
        zookeepersResponse
      ] = await Promise.all([
      getRoutes.getAnimals(),
      getRoutes.getEnclosures(),
      getRoutes.getFeedings(),
      getRoutes.getMedicalRecords(),
      getRoutes.getVeterinars(),
      getRoutes.getVisitors(),
      getRoutes.getZookeepers()
      ])

      items.animals.value = animalsResponse.data
      console.log(items.animals.value)
      items.enclosures.value = enclosuresResponse.data
      items.feedings.value =feedingsResponse.data
      items.medical_records.value = medicalRecordsResponse.data
      items.veterinars.value = veterinarsResponse.data
      items.visitors.value = visitorsResponse.data
      items.zookeepers.value = zookeepersResponse.data
  }

  fetchData()


  // onMounted(async () => {
  //   try {
  //     const response = await axiosInstance.get('AnimalRoutes/getAnimals')
  //     items.animals.value = response.data
  //     console.log(items.animals.value)
  //     // items.animals.value = response.data
  //   } catch (error) {
  //     console.log('hiba')
  //     console.error(error)
  //   }
  // })
  
  const props = defineProps({
    animals: {
      type: Object,
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

<template>
  <div>
    <AnimalsComponent :animals="items.animals" />
    <EnclosuresComponent :enclosures="items.enclosures" />
    <FeedingsComponent :feedings="items.feedings" />
    <MedicalRecordsComponent :medical_records="items.medical_records" />
    <VeterinarsComponent :veterinars="items.veterinars.value" />
    <VisitorsComponent :visitors="items.visitors" />
    <ZookeepersComponent :zookepers="items.zookeepers" />
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
