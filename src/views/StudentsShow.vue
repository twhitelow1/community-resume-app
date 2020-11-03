<template>
  <div class="students-show">
      <div>
        <h1>{{ user.first_name }}</h1>
        <img v-bind:src="user.photo" v-bind:alt="user.first_name"/>
        <button>Contact Info</button><br>
        <span>{{ user.email }}</span>
        <span>{{ user.phone }}</span>
      </div>

      <section id="short-bio">
        <p>{{ user.shortBio }}</p>

      </section>
      
      <section id='experience'>
        <span id="start_date">{{ user.experience.start_date }}</span>
        <span id="end_date">{{ user.experience.end_date }}</span>
        <span id="job_title">{{ user.experience.job_title }}</span>
        <span id="company_name">{{ user.experience.company_name }}</span>
        <span id="details">{{ user.experience.details }}</span>

      </section>
      <section id='education'>
        <span id="start_date">{{ user.education.start_date }}</span>
        <span id="end_date">{{ user.education.end_date }}</span>
        <span id="degree">{{ user.education.degree }}</span>
        <span id="university_name">{{ user.education.university_name }}</span>
        <span id="details">{{ user.education.details }}</span>

      </section>
      <section id='projects'>
        <span id="name">{{ user.projects.name }}</span>
        <span id="description">{{ user.projects.description }}</span>
      
      </section>
      <section id='skills'>
        <span id="name">{{ user.skills.name }}</span>
      
      </section>
      
  </div>
</template>

<style>
img {
  border-radius: 50%;
}
</style>

<script>
import axios from "axios";

export default {
  data: function () {
    return {
      user: {},
    };
  },
  created: function () {
    axios.get("/api/users/" + this.$route.params.id).then(response => {
      console.log("users show", response);
      this.user = response.data;
    });
  },
  methods: {},
};
</script>