<template>
    <div class="button-container">
      <div class="demos-button">
        <a href="#demo-section" @click.prevent="scrollTo('demo-section')">Demo Footage and Media</a>
      </div>
      <div class="demos-button">
        <a href="#resume-section" @click.prevent="scrollTo('resume-section')">Resume</a>
      </div>
    </div>
  </template>
  
  <style scoped>
    /* Button Styles */
    .button-container {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
    }
  
    .demos-button {
      background-color: #595758;
      margin: 2%;
      padding: 12px;
      border-radius: 15px;
      width: 100%;
      transition: background-color 0.3s ease;
    }
  
    .demos-button:hover {
      background-color: #7a7879;
    }
  
    .demos-button a {
      text-decoration: none;
      color: #f2f4ff;
    }
  </style>