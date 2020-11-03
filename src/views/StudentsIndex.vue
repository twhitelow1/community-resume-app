<template>
  <div class="students-index">
    <br />
    <br />
    <h1>All Students</h1>
    <br>
    <br>
    <div class="container">
    <div class="row">
      <div class="col-sm-4" v-for="user in users">
        <div class="card">
          <div class="card-body">
             <img v-bind:src="user.photo" v-bind:alt="user.first_name" />
            <h5 class="card-title">{{ user.first_name }} {{ user.last_name }}</h5>
            <p class="card-text">{{ user.short_bio }}</p>
           <a v-bind:href="'/students/' + user.user_id" class="btn btn-primary">View Resume</a>
          </div>
        </div>
      </div>
    </div>
    </div>
    </div>
</template>

<style>
.students-index {
  background-color: rgb(228, 224, 224);
  /* background: #9cecfb;
  background: -webkit-linear-gradient(to right, #0052d4, #65c7f7, #9cecfb);
  background: linear-gradient(to right, #0052d4, #65c7f7, #9cecfb); */
}

h1 {
  color: gray;
  animation: fade-in 2s ease;
}
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.card {
  margin: 0 auto;
  margin-bottom: 20px;
  border-radius: 10%;
}

.card {
  margin: 0 auto;
  margin-bottom: 20px;
  border-radius: 10%;
}

.card-title {
  font-weight: bold;
}

img {
  border-radius: 50%;
  width: 70%;
  padding: 1em;
  margin-left: 1em;
}

a {
  font-size: 20px;
}
</style>

<script>
// const students = [
//   {
//     firstName: "Prison",
//     lastName: "Mike",
//     email: "prisonmike@theoffice.com",
//     phone: "1234567890",
//     shortBio:
//       "Jim Halpert : What did you do, Prison Mike? Michael Scott : [pretending he went to prison] I stole and I robbed and I kidnapped the President’s son and held him for ransom. Jim Halpert : That is quite the rap sheet, Prison Mike.",
//     linkedInURL: "https://linkedin.com",
//     twitterHandle: "prisonmike",
//     website: "https://website.com",
//     resumeURL: "https://resume.com",
//     github: "https://github.com",
//     photo: "https://pbs.twimg.com/profile_images/1050414908762939393/UKzYsgQg_400x400.jpg",
//   },
// ];

import axios from "axios";

export default {
  data: function () {
    return {
      users: {},
    };
  },
  created: function () {
    axios.get("/api/users").then(response => {
      console.log("users index", response);
      this.users = response.data;
    });
  },
  methods: {},
};
</script>
