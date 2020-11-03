<template>
  <div class="students-show">
      <div>
        <h1>{{ user.first_name}} {{ user.last_name}}</h1>
        <img src="https://pbs.twimg.com/profile_images/1050414908762939393/UKzYsgQg_400x400.jpg" alt="Prison Mike"/>
        <button>Contact Info</button><br>
        <span>prisonmike@theoffice.com</span>
        <span>(123) 456 - 7890</span>
      </div>
      <section id="short-bio">
        Jim Halpert : What did you do, Prison Mike? Michael Scott : [pretending he went to prison] I stole and I robbed and I kidnapped the President’s son and held him for ransom. Jim Halpert : That is quite the rap sheet, Prison Mike.
      </section>
      
      <section id='experience'>
        <span id="start_date">12-12-2018</span>
        <span id="end_date">11-12-2020</span>
        <span id="job_title"></span>
      </section>
      <section id='education'>
      
      </section>
      <section id='projects'>
      
      </section>
      <section id='skills'>
      
      </section>
      
  </div>
</template>

<style>
img {
  border-radius: 50%;
}
</style>

<script>
import { users } from "./data.js";

export default {
  data: function () {
    return {
      users: users,
      user: {},
    };
  },
  created: function () {
    this.user = this.users.find((user) => user.id === parseInt(this.$route.params.id));
    console.log(this.user);
  },
  methods: {},
};
</script>