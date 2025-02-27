<template>
    <div class="video-wrapper">
        <iframe 
            :src="youtubeEmbedUrl" 
            title="YouTube video player" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
            referrerpolicy="strict-origin-when-cross-origin" 
            allowfullscreen
            >
        </iframe>
    </div>

</template>

<script>
    export default {
        name: 'VideoComponent',
        props: {
            youtubeEmbedUrl: {
                type: String,
                default: 'https://www.youtube.com/@blakehphillips'
            }
        }
    }


</script>

<style scoped>
    .video-wrapper {
        position: relative;
        padding-bottom: 56.25%; /* 16:9 aspect ratio */
        height: 0;
        overflow: hidden;
        width: 100%;
    }

    .video-wrapper iframe {
        position: absolute;
        top: 0;
        left: 0;
        width: 95%;
        height: 100%;
        margin: 0 auto;
        right: 0;
        left: 0;    
    }

</style>