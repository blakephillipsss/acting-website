<!--HTML code-->
<template> 
    <div class="main-container">
        <div class="container-one">
            <div class="profile">
                <img src="../assets/Blake H. Phillips Headshot.jpg" alt="" class="">
                <h1>Blake H. Phillips</h1>
                <p>Actor | Writer</p>
            </div>
            <div class="button-container">
                <div class="demos-button">
                    <a href="">Demo Footage and Character Clips</a>
                </div>
                <div class="demos-button">
                    <a href="">Acting Resume</a>
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
                        <p>When Olive Returned (Supporting)</p>
                    </a>
                    <a href="">
                        <img src="../assets/oh_sadie.jpg" alt="">
                        <p>Oh, Sadie! (Supporting)</p>
                    </a>
                    
                </div>
            </div>
            <div class="external-links">
                <h1>Socials</h1>
                <div class="socials">
                    <a href="">
                        <img src="../assets/imdb.png" alt="">
                    </a>
                    <a href="">
                        <img src="../assets/ig.png" alt="">
                    </a>
                    <a href="">
                        <img src="../assets/yt.png" alt="">
                    </a>
                    <a href="">
                        <img src="../assets/li.png" alt="">
                    </a>
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
        background-color: #e4d6d6 ;
        border-radius: 25px;
    }
    .container-one{
        background-color: rgb(130, 184, 255);
        width: 30%;
        padding: .5%;
        border-radius: 25px;
    }
    .profile img{
        height: 40rem;
    }
    .profile p{
        font-size: 1.2rem;
    }
    .button-container{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .demos-button{
        background-color: rgb(59, 144, 255);
        margin: 2%;
        padding: 12px;
        border-radius: 15px;
    }
    .demos-button a{
        text-decoration: none;
        color: #2c3e50;
    }
    .container-two{
        background-color: rgb(184, 247, 226);
        width: 70%;
        margin: 2.5%;
        border-radius: 25px;
    }
    .about-me{
        text-align: left;
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
    }
    .films img{
        height: 25rem;
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
        padding: .5%;
    }
    .socials img{
        height: 2.75rem;
    }
</style>