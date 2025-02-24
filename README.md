# wedsite-
This repositiry contains one wedsite and 2 wed pages 
<!--wed site about the spider man -->
<!--index page ocde-->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spider-Man Index Page</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <div class="logo">🕷️ Spider-Man</div>
        <nav>
            <ul>
                <li><a href="/web_site3/ep_1.html">Homecoming</a></li>
                <li><a href="/web_site3/ep_3.html">Far from home </a></li>
                <li><a href="/web_site3/ep_2.html">no way Home</a></li>
                <li><a href="#">gallary</a></li>
                <li><a href="/web_site3/contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section class="hero">
            <h1>Welcome to the Spider-Man Index Page</h1>
            <p>Explore the amazing world of Spider-Man! From movies to comics, characters to galleries, we've got it all!</p>
        </section>
        <section class="featured-content">
            <div class="content">
                <h2>Featured Movies</h2>
                <div class="image-placeholder"><img src="https://m.media-amazon.com/images/I/81mYx9A9FdL._AC_UF1000,1000_QL80_.jpg" alt ="image" width="500/300"></div>
                <br><br>
                <ul>
                    <li>Spider-Man: Homecoming</li>
                    <li>Spider-Man: Far From Home</li>
                    <li>Spider-Man: No Way Home</li>
                </ul>
            </div>
            <div class="content">
                <h2>Popular Characters</h2>
                <div class="image-placeholder"><img src="https://static1.colliderimages.com/wordpress/wp-content/uploads/2023/07/spider-man-homecoming-tom-holland.jpg"alt="imagae"width="500/300"></div>
                <br><br>
                <ul>
                    <li>Peter Parker</li>
                    <li>Mary Jane Watson</li>
                    <li>Green Goblin</li>
                </ul>
            </div>
        </section>
    </main>
    <br><br><Br>
        <div class="pic">
        <img src="https://www.scribblinggeek.com/wp-content/uploads/2021/12/spider-man-no-way-home-movie-review.jpg"alt="image"width=500/500">
        <img src="https://miro.medium.com/v2/resize:fit:1020/1*cBEw3vCOdWv8dQMoG_EtUA.png"alt="image"width="500/500">
        <img src="https://i.ytimg.com/vi/k-dQlHA-VB8/maxresdefault.jpg"alt="3"width="500/500">
        <img src="https://m.media-amazon.com/images/I/A1QMSfJ4bEL._AC_UF894,1000_QL80_.jpg"alt="4"width="200/300">
    </div>
    <br><br><br><br><br><
    <div class="about">
        <h1>🕷️🕸️🕷️🕸️🕷️🕸️🕷️🕸️ <B>SPIDER MAN</B>🕷️🕸️🕷️🕸️🕷️🕸️🕷️🕸️🕷️</h1>
        <p>
           <font size="5">   Spider-Man 🕷️ is a superhero like no other 🦸‍♂️! After being bitten by a radioactive spider 🕷️, Peter Parker gains amazing powers 🦸‍♂️. He can swing through the streets of New York 🏙️ with his webs 🕸️, crawl up buildings 🧗‍♂️, and his "spider-sense" 🧠 warns him of danger before it happens ⚠️. As Peter 🧑‍🎤, he tries to balance his life as a student 📚, friend 👯‍♂️, and superhero 🦸‍♂️, but it's not always easy 😅. His famous motto, "With great power comes great responsibility" 💪💥, guides him through every challenge 🌟. He faces villains like the Green Goblin 👹, Venom 🐍, and the Vulture 🦅, always ready to protect his beloved city 🏙️. No matter what, Spider-Man always saves the day ⚡! Even if it means making personal sacrifices 💔, he never gives up! 🌟
          
        </font>
        </p>
    </div>
    
<br><br><br><br>
    <footer>
        <p>&copy; 2025 Spider-Man Fan Page. All rights reserved.</p>
    </footer>
</body>
</html>
<!--css for this file-->

body {
    font-family: 'Roboto', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f0f0; 
     color: #333;
/* background-image:url(https://wallpapersmug.com/download/3840x2160/0e57ac/spider-man-neon.jpg);
background-repeat: no-repeat;
background-size: cover; */
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #ff0000;
    color: white;
    padding: 15px 20px;
}

header .logo {
    font-size: 24px;
    font-weight: bold;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    transition: color 0.3s;
}

nav ul li a:hover {
    color: #ffd700;
}

.hero {
    background: url('https://w0.peakpx.com/wallpaper/661/923/HD-wallpaper-chibi-spidey-spiderman-superheroes-digital-art-artwork.jpg') no-repeat center center/cover;
    color: white;
    text-align: center;
    padding: 100px 20px;
}

.hero h1 {
    margin: 0;
    font-size: 48px;
}

.hero p {
    font-size: 24px;
}

.featured-content {
    display: flex;
    justify-content: space-around;
    padding: 40px 20px;
    background-color: white;
    text-align: center;
}

.featured-content .content {
    width: 45%;
}

.featured-content h2 {
    font-size: 32px;
    margin-bottom: 20px;
}

.featured-content ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.featured-content ul li {
    font-size: 20px;
    margin: 10px 0;
}

.featured-content .image-placeholder {
    width: 100%;
    height: 200px;
    background-color: #b80909;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    color: #aaa;
}
.pic{
    width: 100%;
    height: 300px;
    align-content:normal;
    background-color: #b80909;
}
.about {
    background-image: url('https://t4.ftcdn.net/jpg/06/20/96/05/360_F_620960531_UDsMM2MyGwxes4gEFc4Awsb1iYFQksVr.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    /* background:linear-gradient(to right,rgb(124, 3, 3),#943b3b,#3f3d87,rgb(4, 4, 119) ); */
    border: 1px solid #ede7e7;
    border-radius: 50px;
    margin: 15px auto;
    padding: 40px;
    width: 80%;
    box-shadow: 0 0 10px rgb(255, 4, 4);
    color: #f0f0f0;
  }
  .about h2 {
    font-size: 1.8em;
    margin-bottom: 15px;
    justify-content: center;
    text-align: center;
    
  }

footer {
    background-color: #ff0000;
    color: white;
    text-align: center;
    padding: 15px 20px;
    bottom: 0;
    width: 100%;
}
<!--home coming code -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<link rel="stylesheet" type="text/css" href="ep_1.css">
<body>
     <!---header design--->
     <header>
        <a href="#" class="logo">SPIDER<span>man</span></a>
        <ul class="navbar">
            <li><a href="/web_site3/index.html">Home</a></li>
            <li><a href="/web_site3/ep_2.html">Far away home</a></li>
            <li><a href="/web_site3/ep_3.html">no way home</a></li>
            <li><a href="/web_site3/contact.html">Contact us</a></li>
        </ul>
        </header>
        <section class="holiday">
            <div class="holiday-img">
                <img src="https://w0.peakpx.com/wallpaper/86/700/HD-wallpaper-spiderman-homecoming-2017-movie-poster-spider-man-thumbnail.jpg">
            </div>
            <div class="holiday-text"> 
                <h5>Spider Man -HOME COMING </h5>
                <h2> "Spider-Man: Homecoming – Web-Slinging, Teen Drama, and Superhero Adventures 🕷️💥🎒"</h2>
                <p> Sure! Here's the *Spider-Man: Homecoming* description with even more emojis:
                    *Spider-Man: Homecoming* 🕷️🕸️ (2017) is an epic Marvel adventure full of action ⚡, humor 😂, and heart 💖! Peter Parker 🧑‍🦱, a high school student 🎒, struggles to balance his life as a teenager 👦, with his duties as Spider-Man 🕷️. After helping Iron Man 🦾 in *Captain America: Civil War* ⚔️, Peter is eager to prove himself worthy of joining the Avengers 💪. 
                    His chance to shine comes when he faces the villainous Vulture 🦅, who’s wreaking havoc on New York City 🏙️! Peter’s world is filled with action-packed battles 💥, high-tech gadgets ⚙️, and tense moments of danger 🏃‍♂️💨. On top of all that, Peter must deal with the usual teenage dilemmas—friendships 👯‍♂️, schoolwork 📚, and a crush on Liz 😍.               
                    With Tony Stark's guidance 👨‍🔧 and some laughs 🤣 along the way, Peter learns what it truly means to be a hero 🦸‍♂️ and how to take responsibility 🧐. The movie is a mix of excitement 🎢, laughs 😂, and moments that pull at your heartstrings 💖.     A perfect blend of superhero action 🏆, teen drama 🎬, and Marvel magic ✨!</p>
                <a href="#" class="btn">Read more.</a>
            </div>
        </section>
        <br>
        <br>
        <br><BR><BR><BR><BR><br><br><br><br><br>
            <marquee> 
                <img src="https://m.media-amazon.com/images/I/61KqU3T0OcL._AC_UF1000,1000_QL80_.jpg"alt="image2"width="300/500">
                <img src="https://i.redd.it/x9ws3f55079z.jpg"alt="image1" width="300/500">
                <img src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/f21dfd99-c72f-4e7e-8da4-9cf69a1f2049/dfboi0m-74d6f26f-62d4-4a6a-b642-b2157e79a11e.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcL2YyMWRmZDk5LWM3MmYtNGU3ZS04ZGE0LTljZjY5YTFmMjA0OVwvZGZib2kwbS03NGQ2ZjI2Zi02MmQ0LTRhNmEtYjY0Mi1iMjE1N2U3OWExMWUuanBnIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.v6Y1s2enf1ej2iyU9UrBPeBJXofhWksB3ca-wvLxKjo"alt="image3"width="300/500">
                <img src="https://m.media-amazon.com/images/I/919-Tyg91SL._AC_UF350,350_QL80_.jpg"alt="image4"width="300/500"> 
            </marquee>
        <footer>
            <center>
            ©All rights reserved by spider man  2025.
            </center>
           </footer>
        </body>
        </html>
<!--css code for this file -->
*{
    padding:0;
    margin:0;
    box-sizing:border-box;
    list-style:none;
    text-decoration: none;
    border:none;
    outline:none;
    font-family: 'Open sans',sans-serif;
}
:root{
    --text-color:#fff;
    
    --main-color:#f81515;
    --h1-font: 6rem;
    --h2-font: 3 rem;
    --p-font: 5 rem;
}
body{
    color: var(--text-color);
    background-image: url(https://wallpapers.com/images/hd/spider-man-swinging-through-the-city-ghg7nelkrje71krn.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
header{
    position:fixed;
    top:0;
    right:0;
    z-index:1000;
    width: 100%;
    background: transparent;
    padding: 27px 17%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    transition:all .50s ease;
}
.logo{
    font-size:33px;
    color:var(--text-color);
    font-weight: 700;

}
span{
    color:var(--main-color) 

 }
.navbar{
    display:flex;
}
.navbar a{
    color: var(--text-color);
    font-size: var(--p-font);
    font-weight: 500;
    margin: 15px 22px;
    transition: all.50s ease;
}
.navbar a:hover{
    color:var(--main-color)
}
.h-right{
    display: flex;
    align-items:center;
}
.h-right a:first-child{
    color:var(--text-color);
    font-size: var(--p-font);
    margin-right: 20px;
}
.h-right a{
    vertical-align: middle;
    font-size: 20px;
    color:var(--text-color);
    margin-right: 18px;
    margin-left: 5 px;
    transition: all.50s ease;

}
.h-right a:hover{
    color:var(--main-color);
    transform: translateY(-3px);
}
#menu-icon{
    color:var(--text-color);
    font-size: 30px;
    cursor:pointer;
    z-index: 10001;
    display:none;
}
section{
    padding: 70px 17% 60px;
}
.home{
    position: relative;
    height: 100vh;
    width: 100%;
    background-image: linear-gradient(to left,rgba(0,0.0,0.6)rgba(0,0.0,0.3)),url();
    background-size: cover;
    background-position: bottom center;
    display:flex;
    align-items: center;
    justify-content: flex-start;
}
.home-text h5{
    font-size:18px;
    font-weight: 600;
    margin-bottom: 10px;
    text-transform: uppercase;
    letter-spacing: 6px;
    color:var(--main-color);
}
.home-text h1{
    font-size: var(--h1-font);
    font-weight: 800;
    line-height: 1.2;
    margin-bottom: 20px;
}
.home-text p{
    font-size: var(--p-font);
    font-weight: 500;
    line-height: 30px;
    color:#ffffffab;
    margin-bottom: 35px;
}
.btn{
    display: inline-block;
    padding:13px 40px;
    background: var(--main-color);
    color:var(--bg-color);
    font-size: 15px;
    font-weight: 600;
    border:2px solid transparent;
    border-radius:5 px;
    transition: all.50s ease;
    cursor: pointer;
}
.btn:hover{
    transform:translate(10px);
    border:2px solid var(--text-color);
    background:transparent;
    color:var(--text-color);

}
header.sticky{
    padding:8px 17%;
    background:transparent;
    backdrop-filter: blur(35px);
}
.feature-content{
    display:grid;
    grid-template-columns:repeat(auto-fit,min max(150px,auto));
    align-items:center;
    text-align:center;
    gap: 3rem;
}
.row-img{
    overflow:hidden;
    width: 100px;
    height:100px;
    margin: 0 auto;
    margin-bottom:20px;
    border-radius: 50%;
    cursor:pointer;
}
.row-img img{
    width:100%;
    display: block;
    transition: transform 0.7s;
}
.row-img img hover{
    transform:scale(1.2);
}
.feature-content h4{
    font-size: 17px;
    font-weight: 500;
    cursor:pointer;
    transition: all.50s ease;
}
.feature-content h4:hover{
    color: var(--main-color);
}
.holiday{
    display:grid;
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
    gap:9rem;
}
.holiday-img{
    width: 100%;
    height:auto;
    border-radius: 10px;
}
.holiday-text h5{
    font-size: 22px;
    font-weight: 600;
    color:azure;
    text-transform: uppercase;
    letter-spacing: 6px;
    margin-bottom: 20px; 
} 
.holiday-text h2{
    font-size: var(--h2-font);
    font-weight: 800;
    line-height: 1.2;
    margin-bottom:25px;
}
.holiday-text p{
    font-size: var(--p-font);
    font-weight: 500;
    line-height: 30px;
    color:#ffffffab;
    margin-bottom: 35px;
}
.center-text{
    text-align: center;
}
.center-text h2{
    font-size: var(--h2-font);
    font-weight: 800;
}
.tour-content{
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,auto));
    align-items: center;
    gap:3rem;
    margin-top: 5rem;
}
.box{
    position: relative;
}
.box-img{
    width:100%;
    height:100%;
    object-fit: cover;
    border-radius: 10px;
    filter:brightness(70%);
    transition: all.3s cubic-bezier(0.449, 0.05, 0.55, 0.95);
    will-change: filter;
    display:block;
}
.box h6{
    position:absolute;
    left: 25px;
    bottom: 95px ;
    font-size:18px;
    font-weight: 500;
}
.box h4{
    position:absolute;
    left: 25px;
    bottom: 65px ;
    font-size:20px;
    font-weight: 700;
}
.box img:hover{
    filter:brightness(90%) hue-rotate(50 deg);
    transform: scale(1.04);
    cursor:pointer;
}
.center-bt{
    text-align: center;
    margin-top: 4rem;
}
.newsletter-content{
    display:grid;
    grid-template-columns: repeat(2,1fr);
    align-items: center;
    gap:2 rem;
}
.newsletter-text{
    font-size: var(--h2-font);
    font-weight: 800;
    margin-bottom: 150px;
}
.newsletter-text p{
    font-size: var(--p-font);
    font-weight: 500;
    color:#ffffffab;
}
.newsletter-content form{
    display: grid;
    grid-template-columns:1fr 0.4fr;
    gap:1rem;
}
.newsletter-content form input:first-child{
    padding: 15px;
    background: #202020;
    font-size: var(--p-font);
    color:var(--text-color);
    border-radius: 5px;
}  
.footer{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    padding: 20 px;
    grid-template-columns: repeat(auto-fit,minmax(200px,auto));
    gap: 2rem;
}
.footer-box{
    flex:1;
    padding: 20px;
    flex-wrap: wrap;
}
.footer-box h3{
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 15px;

}
.footer-box a{
    color:#979797;
    margin-bottom: 0.8 rem;
    transition: all.50s ease ;
}
.footer-box a:hover{
    transform: translate(-5px);
    color:var(--text-color);
}
.social a{
    display: inline-flex;
align-items: center;
background-color: #202020;
color: var(--text-color);
font-size: 20px;
margin-right: 8px;
}
.social a:hover{
    background: var(--main-color);
    color:var(--bg-color);
    transform:translateX(-4px);
}
.copyright p{
    text-align: center;
    padding: 20px;
    color:#979797;
    font-size: 15px;


}
