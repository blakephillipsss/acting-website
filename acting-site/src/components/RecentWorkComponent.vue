<template>
    <div class="recent-projects">
        <h1>Recently Seen In</h1>
        <div class="films">
            <a :href=WORURL>
                <img :src="require('@/assets/imdb.png')" alt="IMDB" />
            </a>
            <a href="">
                <img src="../assets/WOR.jpg" alt="">
                <p><b>When Olive Returned (Coming Soon!)</b></p>
            </a>
            <a href="">
                <img src="../assets/oh_sadie.jpg" alt="">
                <p><b>Oh, Sadie! (Coming Soon!)</b></p>
            </a>
        </div>
    </div>
</template>

<script>
    export default{
    name: 'RecentWorkComponent',
    props: {}
}
</script>

<style scoped>
    
</style>