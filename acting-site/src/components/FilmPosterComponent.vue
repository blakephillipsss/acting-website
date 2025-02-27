<template>
    <div class="recent-projects">
        <div class="films">
            <a href=filmURL>
                <img :src="require(`@/assets/${filmImage}`)" :alt="filmTitle">
                <p><b>{{filmTitle}}</b></p>
            </a>
        </div>
    </div>
</template>

<script>
    export default{
    name: 'RecentWorkComponent',
    props: {
        filmImage:{
            type: String,
            required: true
        },
        filmTitle:{
            type: String,
            required: true
        },
        filmURL:{
            type: String,
            default: '#'
        }
    }
}
</script>

<style scoped>
.films {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}

.films a {
  text-align: center;
  margin: 1rem;
  text-decoration: underline;
  color: #2c3e50;
  transition: transform 0.3s ease;
}

.films a:hover {
  transform: scale(1.05);
}

.films img {
  height: 20rem;
  padding: 1rem;
  display: block;
  margin: 0 auto;
}
    
</style>