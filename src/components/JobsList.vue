<script setup>
import Job from './Job.vue';

    defineProps(['jobs'])
</script>
<template>
    <article class="job-item" v-for="job in jobs">
        <section>
            <Job :job="job" />
        </section>
    </article>
</template>
<style scoped>
    .job-item {
        padding: 15px;
        border: 2px solid #000;
    margin-bottom: 10px;
    background-color: #fff;
    }
</style>