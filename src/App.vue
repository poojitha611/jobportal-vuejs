<script setup>
import Navbar from './components/Navbar.vue';
import JobsList from './components/JobsList.vue';
import { ref, onMounted} from 'vue';

const jobsList  = ref([]);
  onMounted(() => {
  fetch('https://jobportal-nodejs.onrender.com/api')
    .then(response => response.json())
    .then(res => jobsList.value = res)
})

</script>

<template>
  <header>
    <Navbar />
  </header>
  <main>
    <div class="container">
      <JobsList :jobs="jobsList" />
    </div>
  </main>
</template>

<style scoped>
.container {
  padding: 15px;
  width: 75%;
    margin: auto;
}
header{
  background-color: black;
    color: #fff;
}
</style>