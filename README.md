<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Enoch Deva Kumar | Musician Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Lobster&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css" />
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            color: black;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background-color: #f4f4f9;
        }
        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 90%;
            padding: 20px;
            position: fixed;
            top: 0;
            z-index: 2;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .navbar {
            display: flex;
            justify-content: center;
            flex-grow: 1;
        }
        .navbar a {
            color: black;
            text-decoration: none;
            font-size: 1em;
            margin: 0 15px;
            position: relative;
        }
        .navbar a::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 2px;
            bottom: -3px;
            left: 0;
            background-color: black;
            visibility: hidden;
            transform: scaleX(0);
            transition: all 0.3s ease-in-out;
        }
        .navbar a:hover::after {
            visibility: visible;
            transform: scaleX(1);
        }
        .name {
            font-family: 'Lobster', cursive;
            font-size: 1.8em;
            margin-right: 1%;
            color: black;
        }
        .song-title {
            font-family: 'Lobster', cursive;
            font-size: 2.5em;
            color: #ffcc00;
            margin-top: 100px;
            text-shadow: 2px 2px 4px #000;
            transition: transform 0.3s;
        }
        .song-title a {
            text-decoration: none;
            color: inherit;
            transition: color 0.3s, transform 0.3s;
        }
        .song-title a:hover {
            color: #ff9900;
            transform: scale(1.1);
        }
        .marketing {
            font-size: 1.2em;
            margin-top: 10px;
            text-shadow: 2px 2px 4px #000;
        }
        .listen-button {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 20px;
            font-size: 1.2em;
            color: white;
            background-color: #ffcc00;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            box-shadow: 2px 2px 4px #000;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .listen-button:hover {
            transform: translateY(-5px);
            box-shadow: 4px 4px 8px #000;
        }
        .social-icons {
            display: flex;
            gap: 15px;
        }
        .social-icons img {
            width: 25px;
            height: 25px;
        }
        .quotes {
            font-size: 1.2em;
            color: black;
            padding: 20px;
            max-width: 70%;
            margin: 20px auto;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
            text-shadow: none;
        }
        .self-intro {
            display: flex;
            align-items: center;
            margin: 30px auto;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
            max-width: 80%;
        }
        .self-intro img {
            width: 200px;
            height: auto;
            border-radius: 10%;
            margin-right: 20px;
            box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.7);
        }
        .self-intro p {
            font-size: 1em;
            text-align: left;
            line-height: 1.6;
        }
        .projects-section {
            margin: 40px auto;
            padding: 20px;
            width: 90%;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            text-align: center;
        }
        .projects-title {
            font-family: 'Lobster', cursive;
            font-size: 2em;
            margin-bottom: 20px;
        }
        .swiper {
            width: 100%;
            height: 400px;
            margin: auto;
        }
        .swiper-slide {
            background-position: center;
            background-size: cover;
            width: 350px;
            height: 350px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            transition: transform 0.5s ease, box-shadow 0.5s ease;
            cursor: pointer;
        }
        .swiper-slide:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
        .swiper-button-next, .swiper-button-prev {
            color: #000;
            background-color: #ffcc00;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s, transform 0.3s;
        }
        .swiper-button-next::after, .swiper-button-prev::after {
            font-size: 1.5em;
        }
        .swiper-button-next:hover, .swiper-button-prev:hover {
            background-color: #ff9900;
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="name">Enoch Deva Kumar</div>
        <div class="navbar">
            <a href="#home">Home</a>
            <a href="#contact">Contact</a>
            <a href="#teams">Teams</a>
        </div>
        <div class="social-icons">
            <a href="https://instagram.com/yourprofile" target="_blank">
                <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram Logo">
            </a>
            <a href="https://facebook.com/yourprofile" target="_blank">
                <img src="https://upload.wikimedia.org/wikipedia/commons/5/51/Facebook_f_logo_%282019%29.svg" alt="Facebook Logo">
            </a>
        </div>
    </div>
    <div class="content">
        <div class="song-title">
            <a href="https://link-to-your-song.com" target="_blank">Enoch</a>
        </div>
        <div class="marketing">
            <p>Composer | Singer | Multi-instrumentalist | Audio Engineering</p>
            <a href="https://link-to-your-song.com" target="_blank" class="listen-button">Let's connect!</a>
        </div>
    </div>
    <div class="quotes">
        "The only way to do great work is to love what you do. If you haven't found it yet, keep looking. Don't settle." – Steve Jobs
    </div>
    <div class="self-intro">
        <img src="https://cdn.pixabay.com/photo/2020/06/26/14/46/india-5342927_960_720.jpg" alt="Your Image">
        <p>Hello! I'm Enoch Deva Kumar, a passionate musician dedicated to creating beautiful melodies and harmonies. With years of experience in composition, performance, and audio engineering, I strive to deliver music that resonates with the soul. Join me on this musical journey, and let's create something extraordinary together.</p>
    </div>

    <div class="projects-section">
        <div class="projects-title">My Projects</div>
        <div class="swiper">
            <div class="swiper-wrapper">
                <div class="swiper-slide" style="background-image: url('https://img.youtube.com/vi/VIDEO_ID_1/hqdefault.jpg')" onclick="window.open('https://www.youtube.com/watch?v=VIDEO_ID_1', '_blank')"></div>
                <div class="swiper-slide" style="background-image: url('https://img.youtube.com/vi/VIDEO_ID_2/hqdefault.jpg')" onclick="window.open('https://www.youtube.com/watch?v=VIDEO_ID_2', '_blank')"></div>
                <div class="swiper-slide" style="background-image: url('https://img.youtube.com/vi/VIDEO_ID_3/hqdefault.jpg')" onclick="window.open('https://www.youtube.com/watch?v=VIDEO_ID_3', '_blank')"></div>
                <div class="swiper-slide" style="background-image: url('https://img.youtube.com/vi/VIDEO_ID_4/hqdefault.jpg')" onclick="window.open('https://www.youtube.com/watch?v=VIDEO_ID_4', '_blank')"></div>
                <div class="swiper-slide" style="background-image: url('https://img.youtube.com/vi/VIDEO_ID_5/hqdefault.jpg')" onclick="window.open('https://www.youtube.com/watch?v=VIDEO_ID_5', '_blank')"></div>
                <div class="swiper-slide" style="background-image: url('img6.jpg')"></div>
                <div class="swiper-slide" style="background-image: url('img7.jpg')"></div>
                <div class="swiper-slide" style="background-image: url('img8.jpg')"></div>
            </div>
            <div class="swiper-button-next"></div>
            <div class="swiper-button-prev"></div>
        </div>
    </div>

    <script src="https://unpkg.com/swiper/swiper-bundle.min.js"></script>
    <script>
        var swiper = new Swiper(".swiper", {
            effect: "coverflow",
            grabCursor: true,
            centeredSlides: true,
            slidesPerView: 3,
            speed: 600,
            coverflowEffect: {
                rotate: 50,
                stretch: 0,
                depth: 100,
                modifier: 1,
                slideShadows: true,
            },
            loop: true,
            autoplay: {
                delay: 2500,
                disableOnInteraction: false,
            },
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },
        });

        document.querySelectorAll('.swiper-slide').forEach((slide, index) => {
            slide.dataset.index = index;
            slide.addEventListener('click', () => {
                swiper.slideTo(slide.dataset.index);
            });
        });

        var isDragging = false;

        swiper.on('touchStart', function() {
            isDragging = false;
        });

        swiper.on('touchMove', function() {
            isDragging = true;
        });

        swiper.on('touchEnd', function() {
            if (isDragging) {
                isDragging = false;
                return;
            }
            swiper.slideTo(swiper.clickedIndex);
        });
    </script>
</body>
</html>
