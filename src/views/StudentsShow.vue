<template>
  <div class="students-show">
      <div>
        <h1>Prison Mike</h1>
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
    first_name: "Bob",
    last_name: "Smith",
    email: "prisonmike@theoffice.com",
    phone_number: "1234567890",
    short_bio:
      "Jim Halpert : What did you do, Prison Mike? Michael Scott : [pretending he went to prison] I stole and I robbed and I kidnapped the President’s son and held him for ransom. Jim Halpert : That is quite the rap sheet, Prison Mike.",
    linkedin_url: "https://linkedin.com",
    twitter_handle: "prisonmike",
    website_url: "https://website.com",
    online_resume_url: "https://resume.com",
    github_url: "https://github.com",
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