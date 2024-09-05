<!-- ProfileComponent.vue -->
<template>
  <div class="profile">
    <h1>{{ name }}</h1>
    <p>{{ pronouns }}</p>
    <img :src="require('@/assets/Blake H. Phillips Headshot.jpg')" alt="Blake H. Phillips" />
    <p>{{ title }}</p>
    <a :href="'mailto:' + email">{{ email }}</a>
    <p>{{ phone }}</p>
  </div>
</template>

<script>
  export default {
    name: 'ProfileComponent',
    props: {
      name: {
        type: String,
        default: 'Blake H. Phillips'
      },
      pronouns: {
        type: String,
        default: '(he/him/his)'
      },
      title: {
        type: String,
        default: 'Non-Union Toronto Actor'
      },
      email: {
        type: String,
        default: 'acting@blakehphillips.com'
      },
      phone: {
        type: String,
        default: '+1 (416) 818-1158'
      }
    }
  }
</script>
  
  <style scoped>
    /* Profile Styles */
    .profile h1 {
      color: #f2f4ff;
      font-family: "Bodoni MT Condensed", serif;
      font-size: 2.8rem;
    }
  
    .profile img {
      height: auto;
      max-width: 100%;
    }
  
    .profile p, .profile a {
      color: #f2f4ff;
    }
  
    .profile p {
      font-size: 1.2rem;
    }
  
    .profile a {
      text-decoration: underline;
    }
  </style>