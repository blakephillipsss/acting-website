<!--HTML code-->
<template> 
    <div class="main-container">
        <div class="container-one">
            <div class="profile">
                <img src="../assets/headshot.jpg" alt="" class="">
                <h1>Blake H. Phillips</h1>
                <p>Actor | Writer</p>

            </div>
            <div class="external-links">
                <a href="">
                    <div class="link">
                        <img src="../assets/imdb.png" alt="">
                        <h2>IMDB</h2>
                        
                    </div>
                    <div class="link">
                        <img src="../assets/ig.png" alt="">
                        <h2>Instagram</h2>
                        
                    </div>
                    <div class="link">
                        <img src="../assets/yt.png" alt="">
                        <h2>Youtube</h2>
                        
                    </div>
                    <div class="link">
                        <img src="../assets/li.png" alt="">
                        <h2>LinkedIn</h2>
                        
                    </div>
                </a>
            </div>
        </div>
        <div class="container-two">
            <div class="about-me">
                <h1>About Blake</h1>
                <p>Blake H. Phillips is an emerging talent in the world of acting and writing, driven by a passion for storytelling and a commitment to exploring the human condition. With a dedication to his craft, Blake is rapidly making a name for himself as a versatile actor capable of delivering powerful performances across a range of genres. 
                    As an actor, Blake immerses himself in each role, bringing characters to life with authenticity and depth. His ability to convey complex emotions and connect with audiences has earned him recognition and praise in the industry. Whether portraying a dramatic lead or adding a touch of humor to a scene, Blake's performances are marked by a genuine enthusiasm and a strong work ethic.
                    In addition to his acting endeavors, Blake is also an accomplished writer. His writing journey is fueled by a deep love for crafting narratives that resonate with readers and viewers alike. Through his writing, Blake aims to evoke emotions, provoke thought, and inspire change, creating stories that leave a lasting impact.
                    Blake H. Phillips believes in the transformative power of storytelling and is dedicated to contributing meaningful work to the entertainment industry. As he continues to grow and evolve in his career, Blake looks forward to collaborating with fellow artists, learning from each experience, and making a significant impact through his art.
                    Join Blake on his exciting journey as he strives to make his mark as both an actor and a writer, sharing incredible stories with the world.</p>
            </div>
            <div class="recent-projects">
                <h1>Recent Seen In</h1>
                <div class="films">
                    <img src="oh_sadie.png" alt="Oh, Sadie Poster">
                    <img src="WOR.png" alt="When Olive Returned Poster">
                </div>
            </div>
            <div class="button-container">
                <div class="clips-and-demos">
                    <a href="">Demo Footage and Character Clips</a>
                </div>
                <div>
                    <a href="">Acting Resume</a>
                </div>
            </div>
        </div>
    </div>
    
</template>

<!--JS code-->
<script>
export default {

}

</script>

<!--CSS code-->
<style scoped>
    img{
        height:20px;
    }
    .main-container{
        display: flex;
        flex-direction: row;
        background-color: #ffffff ;
    }
    .container-one{
        background-color: blue;
    }
    .container-two{
        background-color: aquamarine;
    }
</style>