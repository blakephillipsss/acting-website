<!--HTML code-->
<template>
    <head><title>Blake H. Phillips</title></head>
    <div class="main-container">
        <div class="container-one">
            <div class="profile">
                <h1>Blake H. Phillips</h1>
                <img src="../assets/Blake H. Phillips Headshot.jpg" alt="" class="">
                <p>Non-Union Toronto Actor</p>
                <a href="mailto:actor@blakehphillips.com">actor@blakehphillips.com</a>
                <p>+1 (416) 818-1158</p>
            </div>
            <div class="button-container">
                <div class="demos-button">
                    <a href="">Demo Footage and Clips</a>
                </div>
                <div class="demos-button">
                    <a href="">Resume</a>
                </div>
            </div>
            <div class="external-links">
                <div class="socials">
                    <a href="">
                        <img src="../assets/imdb.png" alt="">
                    </a>
                    <a href="https://www.instagram.com/blakehphillips/">
                        <img src="../assets/ig.png" alt="">
                    </a>
                    <a href="https://www.youtube.com/@blakehphillips">
                        <img src="../assets/yt.png" alt="">
                    </a>
                    <a href="https://www.linkedin.com/in/bhp42/">
                        <img src="../assets/li.png" alt="">
                    </a>
                </div>
            </div>
            
        </div>
        <div class="container-two">
            <div class="about-me">
                <h1>About Blake</h1>
                <p>Blake H. Phillips is an emerging talent in the world of acting and writing, driven by a passion for storytelling and a commitment to exploring the human condition. With a dedication to his craft, Blake is rapidly making a name for himself as a versatile actor capable of delivering powerful performances across a range of genres. 
                    Join Blake on his exciting journey as he strives to make his mark as both an actor and a writer, sharing incredible stories with the world.</p>
            </div>
            <div class="recent-projects">
                <h1>Recent Seen In</h1>
                <div class="films">
                    <a href="">
                        <img src="../assets/WOR.jpg" alt="">
                        <p><b>When Olive Returned (Supporting)</b></p>
                    </a>
                    <a href="">
                        <img src="../assets/oh_sadie.jpg" alt="">
                        <p><b>Oh, Sadie! (Supporting</b>)</p>
                    </a>
                </div>
            </div>
        </div>
        <div class="container-three">
            <div class="youtube-video">
                <h1>Demo and Media</h1>
                <!-- Embed YouTube Videos -->
                <iframe width="560" height="315" src="https://www.youtube.com/embed/wIjbAvhwO1k?si=XfR5-tNOVJi8AJcd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
        <div class="container-four">
            <div class="pdfs">
                <h1>Resume</h1>
                <!-- Embed PDF -->
                <iframe src="../../public/Blake H. Phillips Resume.pdf" width="100%" height="500px">pdf</iframe>
                 <!-- <object data="../assets/Blake H. Phillips Resume.pdf" class="pdf" width="100%" height="500px"></object> -->
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
        flex-wrap: wrap;
        justify-content: space-around;
        background-color: #96C5F7  ;
        border-radius: 25px;
        width: 100%;
    }
    .container-one, .container-two, .container-three, .container-four{
        flex: 1;
        min-width: 350px;
        margin: 10px;
    }
    .container-one{
        background-color: #304C89;
        max-width: 30%;
        padding: 1%;
        border-radius: 25px;
        margin: .5%;
        margin-top: 2%;
    }
    .profile h1{
        color: #f2f4ff;
        font-family: "Bodoni MT Condensed", serif;
        font-size: 2.8rem;
    }
    .profile img{
        height: auto;
        max-width: 100%;
    }
    .profile p{
        color: #f2f4ff;
        size: 1.2rem;
    }
    .profile a{
        text-decoration: underline;
        color: #f2f4ff;
    }
    .button-container{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }
    .demos-button{
        background-color: #595758;
        margin: 2%;
        padding: 12px;
        border-radius: 15px;
        width: 100%;
    }
    .demos-button a{
        text-decoration: none;
        color: #f2f4ff;
        align-items: center;
        justify-content: center;
    }
    .container-two{
        background-color: #F2F4FF;
        max-width: 34%;
        margin: 0.5%;
        border-radius: 25px;
    }
    .about-me h1{
        text-align: center;
    }
    .about-me p{
        text-align: justify;
        margin: 2%;
    }
    .films{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
    }
    .films a{
        text-align: center;
        margin: 1rem;
        text-decoration: underline;
        color: #2c3e50;
    }
    .films img{
        height: 20rem;
        padding: 1rem;
        display: block;
        margin: 0 auto;
    }
    .socials{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }
    .socials a{
        margin-top: 3%;
        padding: .5%;
    }
    .socials img{
        height: 2.75rem;
    }
    .container-three{
        background-color: #F2F4FF;
        width: 36%;
        margin: 0.5%;
        border-radius: 25px;
    }
    .container-three iframe{
        max-width: 100%;
        height: auto;
    }
</style>