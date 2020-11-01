<template>
  <div class="students-index">
    <div v-for="student in students">
      <h1>All Students</h1>
      <div >
        <img v-bind:src="student.photo" v-bind:alt="student.firstName"/>
        <h2> {{ student.firstName}}  {{ student.lastName}}</h2>
        <p>{{ student.shortBio}}</p>
        <button>View Resume</button>
      </div>
    </div>
  </div>
</template>

<style>
img {
  border-radius: 50%;
}
</style>

<script>
const students = [
  {
    firstName: "Prison",
    lastName: "Mike",
    email: "prisonmike@theoffice.com",
    phone: "1234567890",
    shortBio:
      "Jim Halpert : What did you do, Prison Mike? Michael Scott : [pretending he went to prison] I stole and I robbed and I kidnapped the President’s son and held him for ransom. Jim Halpert : That is quite the rap sheet, Prison Mike.",
    linkedInURL: "https://linkedin.com",
    twitterHandle: "prisonmike",
    website: "https://website.com",
    resumeURL: "https://resume.com",
    github: "https://github.com",
    photo: "https://pbs.twimg.com/profile_images/1050414908762939393/UKzYsgQg_400x400.jpg",
  },
  {
    firstName: "Bob",
    lastName: "Smith",
    email: "prisonmike@theoffice.com",
    phone: "1234567890",
    shortBio:
      "Jim Halpert : What did you do, Prison Mike? Michael Scott : [pretending he went to prison] I stole and I robbed and I kidnapped the President’s son and held him for ransom. Jim Halpert : That is quite the rap sheet, Prison Mike.",
    linkedInURL: "https://linkedin.com",
    twitterHandle: "prisonmike",
    website: "https://website.com",
    resumeURL: "https://resume.com",
    github: "https://github.com",
    photo: "https://pbs.twimg.com/profile_images/1050414908762939393/UKzYsgQg_400x400.jpg",
  },
  {
    firstName: "John",
    lastName: "Mike",
    email: "prisonmike@theoffice.com",
    phone: "1234567890",
    shortBio:
      "Jim Halpert : What did you do, Prison Mike? Michael Scott : [pretending he went to prison] I stole and I robbed and I kidnapped the President’s son and held him for ransom. Jim Halpert : That is quite the rap sheet, Prison Mike.",
    linkedInURL: "https://linkedin.com",
    twitterHandle: "prisonmike",
    website: "https://website.com",
    resumeURL: "https://resume.com",
    github: "https://github.com",
    photo: "https://pbs.twimg.com/profile_images/1050414908762939393/UKzYsgQg_400x400.jpg",
  },
];

export default {
  data: function () {
    return {
      students: students,
    };
  },
  created: function () {},
  methods: {},
};
</script>