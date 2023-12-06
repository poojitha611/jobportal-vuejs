<script setup>
    defineProps(['job'])
</script>
<template>
    <div class="">
        <h3 class="job_title">{{ job.job_title }}</h3>
        <p class="com-name">{{ job.company_name }}</p>
        <p class="exp-sal">
            <span><i class="fa fa-suitcase" aria-hidden="true"></i></span>{{ job.experience }} | 
            <span><i class="fa fa-usd" aria-hidden="true"></i></span>{{ job.salary_range }} |
            <span><i class="fa fa-map-marker" aria-hidden="true"></i></span>{{ job.location }}
        </p>
        <p class="job_desc"><span><i class="fa fa-file-text-o" aria-hidden="true"></i></span>{{ job.job_description }}</p>
        <p class="skills">{{ job.skills }}</p>
        <hr />
        <div class="footer">
            <p class="date">{{ job.job_posted_date }}</p>
            <button class="apply-btn">Apply Now</button>
        </div>
    </div>
</template>
<style scoped>
    .job_title {
        font-weight: bold;
        font-size: 20px;
    }
    .com-name {
        font-weight: 600;
        margin-bottom: 10px;
    }
    span{
        padding-right: 10px
    }
    .exp-sal {
        color: #474d6a;
    font-size: 14px;
    margin-bottom: 10px;
    font-weight: 500;
    }
    .job_desc {
        overflow: hidden;
    display: inline-block;
    white-space: nowrap;
    text-overflow: ellipsis;
    width: 100%;
    font-size: 14px;
    }
    .skills{
        font-size: 14px;
        margin-bottom: 10px;
    }
    .date{
        margin-top: 5px;
        font-size: 11px;
    }
    .footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .apply-btn {
        border: unset;
        margin-top: 5px;
        padding: 10px 15px;
        font-size: 11px;
        border-radius: 10px;
        background-color: #000;
        color: #fff;
        cursor: pointer;
    }
</style>