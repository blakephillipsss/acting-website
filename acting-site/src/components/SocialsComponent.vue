<template>
    <div class="external-links">
        <div class="socials">
            <a :href=imdbURL>
                <img :src="require('@/assets/imdb.png')" alt="IMDB" />
            </a>
            <a :href=igURL>
                <img :src="require('@/assets/ig.png')" alt="Instagram" />
            </a>
            <a :href=ytURL>
                <img :src="require('@/assets/yt.png')" alt="Youtube" />
            </a>
            <a :href=liURL>
                <img :src="require('@/assets/li.png')" alt="LinkedIn" />
            </a>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'SocialsComponent',
    props: {
      imdbURL: {
        type: String,
        default: 'https://www.imdb.com/name/nm16436371/?ref_=ttfc_fc_cl_t11'
      },
      igURL: {
        type: String,
        default: 'https://www.instagram.com/blakehphillips/'
      },
      ytURL: {
        type: String,
        default: 'https://www.youtube.com/@blakehphillips'
      },
      liURL: {
        type: String,
        default: 'https://www.linkedin.com/in/bhp42/'
      }
    }
    }

</script>

<style scoped>
.socials {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

.socials a {
  margin-top: 3%;
  padding: .5%;
  transition: transform 0.3s ease;
}

.socials a:hover {
  transform: scale(1.1);
}

.socials img {
  height: 2.75rem;
}
</style>