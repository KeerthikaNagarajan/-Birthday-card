# Ex-09:
## Create a Birthday card using HTML and CSS
### AIM:
The aim of the provided HTML and CSS code is to create a birthday card with animations and a surprise gift.
### ALGORITHM:
1. Create HTML files: card.html, index.html, and link.html.
2. Define CSS styles for various elements and animations.
3. Customize the background images and text content in each HTML file.
4. Use marquee tags, CSS animations, and image alignments to create dynamic effects.
5. Add audio to the index.html file using the audio tag.
6. Create a link to navigate from link.html to card.html and add a hovering animation effect to the image.
### PROGRAM:
#### card.html
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Hi!</title>
  </head>
  <style>
    body, html {
	  height: 100%;
	  margin: 0;
	}
    .container {
	  height: 100%;
	}
    marquee{
        font-size: 25px;
            padding-top: 1%;
			margin: 0;
            font-family:Georgia, 'Times New Roman', Times, serif;
            font-weight: 800;
			animation-name: color-change;
			animation-duration: 5s;
			animation-iteration-count: infinite;
			animation-direction: alternate;
			animation-timing-function: ease-in-out;
    }
    p{
            font-size: 45px;
            padding-top: 5%;
			margin: 0;
            font-family:Georgia, 'Times New Roman', Times, serif;
            font-weight: 800;
			animation-name: color-change;
			animation-duration: 5s;
			animation-iteration-count: infinite;
			animation-direction: alternate;
			animation-timing-function: ease-in-out;
		}
    @keyframes color-change {
			0% {
				color: #3f3124;
			}

			50% {
				color: #ea2c0f;
			}

			100% {
				color: #0090e3;
			}
  }
  @keyframes move-up {
    from {
      transform: translateY(90%); 
    }
    to {
      transform: translateY(0%); 
    }
  }

  .move-me {
    animation: move-up 4s linear infinite; 
  }
  .centered-image {
    position: absolute;
    top: 60%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .bg {
      height: 100%;
	  background-position: center;
	  background-repeat: no-repeat;
	  background-size: cover;
	  background-attachment: fixed;
	  
   }
  .image1 {
	  background-image: url("hot-air-balloon-wallpaper.gif");
	}
  </style>
  <body>
    <div class="container">
        <div class="bg image1">
            <marquee>🥳❤️🎉 Wishing you a day filled with happiness and a year filled with joy. Happy birthday! 🎉❤️🥳</marquee>
            <div><p align="center">HAPPY BIRTHDAY!!</p></div>
            <img align="left" class="move-me" src="b1.png"/><img align="right" class="move-me" src="b1.png" />
            <a href="index.html"><img class="centered-image" src="caki.png" alt="Caki"></a>
        </div>
  </body>
</html>
```
### index.html
```html
<!DOCTYPE html>
<html>
  <head>
    <title>❤️</title>
  </head>
  <style>
body, html {
	  height: 100%;
	  margin: 0;
	}
  h1 {
			margin: 0;
			animation-name: color-change;
			animation-duration: 5s;
			animation-iteration-count: infinite;
			animation-direction: alternate;
			animation-timing-function: ease-in-out;
		}
	.container {
	  height: 100%;
	}
   .bg {
      height: 100%;
	  background-position: center;
	  background-repeat: no-repeat;
	  background-size: cover;
	  background-attachment: fixed;
	  
   }
  .image1 {
	  background-image: url("balloonsss.gif");
	}
	.image2 {
	  background-image: url("gift.gif");
	}
  .image3 {
    background-image: url("bal.png");
  }
  #bottom {
        position: absolute;
        bottom: 0;
      }
  .center {
      display: block;
      margin-left: 30%;
      margin-right: 30%;
      width: 55%;
}
@keyframes color-change {
			0% {
				color: #fff;
			}

			50% {
				color: #000000;
			}

			100% {
				color: #ffffff;
			}
  }  
  </style>
  <body>
    <body>
      <div class="container">
      <div class="bg image1">
        <audio controls autoplay>
          <source src="audiohb.ogg" type="audio/ogg">
          <source src="audiohb.mp3" type="audio/mpeg">
        </audio>
        <h1 align="center">Hello!!</h1>
        <div id="bottom"><h1>Scroll Down Please!! </h1></div>
      </div>
      <div class="bg image2">
        <h1 align="center">I have a surprise for You </h1>
      </div>
      <div class="bg image3">
        <h1 align="center" >HAPPY BIRTHDAY NITHISH!!</h1>
        <img src="nini.png" class="center">
        <div style="margin-left: 30%; margin-right: 30%; position: absolute;"><h1 >HAVE A GREAT YEAR AHEAD!!</h1></div>
    </div>
    </div>
    

  </body>
</html>

```
### link.html
```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Hello</title>
    <style>
        img:hover {
  animation: shake 0.5s;
  animation-iteration-count: infinite;
}
@keyframes shake {
  0% { transform: translate(1px, 1px) rotate(0deg); }
  10% { transform: translate(-1px, -2px) rotate(-1deg); }
  20% { transform: translate(-3px, 0px) rotate(1deg); }
  30% { transform: translate(3px, 2px) rotate(0deg); }
  40% { transform: translate(1px, -1px) rotate(1deg); }
  50% { transform: translate(-1px, 2px) rotate(-1deg); }
  60% { transform: translate(-3px, 1px) rotate(0deg); }
  70% { transform: translate(3px, 1px) rotate(-1deg); }
  80% { transform: translate(-1px, -1px) rotate(1deg); }
  90% { transform: translate(1px, 2px) rotate(0deg); }
  100% { transform: translate(1px, -2px) rotate(-1deg); }
}
    </style>
    </head>
    <body style="background-color:cadetblue">
    <body>
        <a href="card.html"><img style="padding-right: 50%;padding-left: 50%; padding-top: 10%;"src="gitfi.png" width="300" height="300"/></a>
        <h1 align="right" style="padding-right: 40%;">OPEN THE GIFT ❤️</h1>
    </body>
</html>
```
### OUTPUT:
#### card.html
<img width="523" alt="image" src="https://github.com/KeerthikaNagarajan/Birthday-card/assets/93427089/aa44bd9b-d62f-41de-9301-4c6ea8f2fb8d">

#### index.html
<img width="523" alt="image" src="https://github.com/KeerthikaNagarajan/Birthday-card/assets/93427089/96e8df82-2e75-4960-affe-9881d6256b8f">

#### link.html
<img width="463" alt="image" src="https://github.com/KeerthikaNagarajan/Birthday-card/assets/93427089/5a8bb6ed-c9a7-401f-b6e8-590df30c8983">

<img width="464" alt="image" src="https://github.com/KeerthikaNagarajan/Birthday-card/assets/93427089/a5ceea87-121c-409a-abad-a68eee962381">

<img width="461" alt="image" src="https://github.com/KeerthikaNagarajan/Birthday-card/assets/93427089/2722b747-4795-4bee-841c-e9efe20a4213">

#### Video:
https://github.com/KeerthikaNagarajan/Birthday-card/assets/93427089/48f72786-2584-477d-8f42-25694db245d7

### RESULT:
The code will provide a birthday card with animations and a surprise gift.
