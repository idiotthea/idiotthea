<!DOCTYPE html>
<html lang="en" >
<head>
  <meta charset="UTF-8">
  <title>For You</title>
  <link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet"><link rel="stylesheet" href="./style.css">

</head>
<body>
<!-- partial:index.partial.html -->
<body>
  <article>
    <div class="envelope-container">
      <div class="message message-1" id="message-1">
        <h1>Dear Waleed,
            I'm so glad that you're in my life. You make everything tranquil to live in this cruel world. 
            I never thought I could find a home in you, but you proved me wrong.
            I value our friendship so much because I don't want to lose anything that we have or anything
            that we've shared. I couldn't handle it if you left me.
            I'm not fully trusting you, but from my perspective, you have good intentions. 
            I appreciate every effort you make for me, even if it hurts you repeatedly. 
            Because of that, you've earned my trust in some way. I'm scared our friendship might change, 
            so I'm careful not to give it away too simply.
            Thank you for being there for me. I hope we can continue to grow and learn from each other.</h1>
        <p>Sending a little something for you more...</p>
      </div>
      <div class="message message-2" id="message-2">
        <h2>Dear Waleed,
            I'm sorry that I can't fully express my feelings because it's hard to find the right words. 
            Ever since we connected, I knew that I could fall in love with you. And then my words became
            a reality because I had already fallen in love with you before I knew it— just in denial.
            I still felt the pain in your heart when you mentioned the name of the girl you love—one you 
            cherish and admire. And because of that, I'm afraid to trust you with my feelings.
            That's why I keep distancing myself from you.
            I wrote this letter not to confess but to let you know why I'm pulling away from you.</h2>
      </div>
      <button class="close-btn" id="close-btn" onclick="toggleEnvelope()">close envelope</button>
      <button class="heart-btn" id="heart-btn" onclick="toggleEnvelope()">&#10084;
        <span class="heart-btn-text">click</span>
      </button>
      <div class="envelope-flap">
        <svg class="inner">
          <polygon class="inner-polygon" id="inner-polygon" points="5,0 345,0 175,145" ></polygon>
        </svg>
        <svg class="outer" id="outer">
          <polygon class="outer-polygon" points="5,150 345,150 175,0"></polygon>
        </svg>
        <div class="floating-hearts">
          <div class="hearts-row row-10">
            <div>
              <i class="ri-heart-fill"></i>
            </div>
          </div>
          <div class="hearts-row row-9">
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
          </div>
          <div class="hearts-row row-8">
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
          </div>
          <div class="hearts-row row-7">
            <div><i class="ri-heart-fill"></i></div>            
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
          </div>
          <div class="hearts-row row-6">
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
          </div>
          <div class="hearts-row row-5">
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
          </div>
          <div class="hearts-row row-4">
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
          </div>
          <div class="hearts-row row-3">
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
          </div>
          <div class="hearts-row row-2">
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
            <div><i class="ri-heart-fill"></i></div>
          </div>
          <div class="hearts-row row-1">
            <div><i class="ri-heart-fill"></i></div>
          </div>
        </div>
      </div>
      <div class="envelope-base"></div>
    </div>
  </article>  
</body>
<!-- partial -->
  <script  src="./script.js"></script>

</body>
</html>
 20 changes: 20 additions & 0 deletions20  
letter/script.js
@@ -0,0 +1,20 @@
const innerPolygon = document.getElementById("inner-polygon");
const outer = document.getElementById("outer");
const closeBtn = document.getElementById("close-btn");
const message1 = document.getElementById("message-1");
const message2 = document.getElementById("message-2");
const heartsRow = document.querySelectorAll(".hearts-row");
const heartBtn = document.getElementById("heart-btn");

function toggleEnvelope() {

  innerPolygon.classList.toggle("inner-open");
  outer.classList.toggle("outer-open");
  heartBtn.classList.toggle("hide");
  closeBtn.classList.toggle("show");
  message1.classList.toggle("hide");
  message2.classList.toggle("show");

  heartsRow.forEach(element => element.classList.toggle("animated"));

}
@import url('https://fonts.googleapis.com/css2?family=Lobster&display=swap');

/* RESET */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
:root {
  /* COLORS */
  --red-dk: #BA0025;
  --red-md: #DC143C;
  --pink-dk: #EB0674;
  --pink-lt: #FFB6C1;
  --purple-dk: #98006A;
  --purple-md: #CE0090;

  --neutral-dk: #333;
  --neutral-md: #999;
  --neutral-mdlt: lightgray;
  --neutral-lt: #fff;
  /* FONT */
  --font-sans: "Poppins", sans-serif;
  --font-display: "Lobster", sans-serif;
}

/* MAIN STYLES */
body {
  background: var(--pink-lt); 
  font-family: var(--font-sans);
}
p {
  font-size: 20px;
  margin: 20px 0;
}
h1, h2 {
  font-family: var(--font-display);
  font-size: 36px;
  color: var(--red-dk);
  text-shadow: 1px 2px 2px white;
}
button {
  background: transparent;
  border: none;
  font-family: var(--font-sans);
  cursor: pointer;
}
/* this article is used to center the component within the viewport */
article {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  width: 100%;
}

/* MESSAGES */
.message {
  text-align: center;
  margin-top: 40px;
}
.message-2 {
  display: none;
}

/* ENVELOPE */

/* envelope-container contains all elements of the featured component (you can think of it like your canvas area) */
.envelope-container {
  position: relative; /* needed to allow for positioning some elements as absolute within the container */
  height: 450px;
  width: 350px;
}
.envelope-base {
  position: absolute;
  bottom: 0;
  height: 200px;
  width: 100%;
  border: 1px solid var(--neutral-md);
  border-radius: 5px;
  background: var(--neutral-lt);
  box-shadow: 0px 10px 30px rgba(0,0,0,.3), 0px 8px 10px rgba(0,0,0,.3);
  z-index: 1;
}
.envelope-flap {
  position: absolute;
  bottom: 50px;
  height: 300px;
  width: 100%;
  z-index: 10;
}
.inner {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 50%;
  width: 100%;
}
.inner-polygon {
  fill: var(--neutral-lt); 
  stroke: var(--neutral-md); 
  stroke-width: 1;
}
.inner-open {
  fill: var(--neutral-mdlt);
}
.outer {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0;
  overflow: hidden;
}
.outer-polygon {
  fill: var(--neutral-lt); 
  stroke: var(--neutral-md); 
  stroke-width: 1;
}
.outer-open {
  opacity: 1;
}

/* HEART BUTTON */
.heart-btn {
  position: absolute;
  display: flex;
  align-items: center;
  justify-content: center;
  bottom: 20px;
  left: 145px;
  color: var(--red-md);
  font-size: 60px;
  z-index: 1000;
}
.heart-btn:hover {
  color: var(--purple-dk);
}
.heart-btn-text {
  position: absolute;
  font-size: 12px;
  letter-spacing: .5px;
  color: var(--neutral-lt);
  z-index: 1000;
}
/* CLOSE BUTTON */
.close-btn {
  position: absolute;
  bottom: 10px;
  left: 10px;
  color: var(--neutral-dk);
  background: var(--pink-lt);
  border: none;
  border-radius: 5px;
  padding: 8px 16px;
  box-shadow: 0px 2px 6px rgba(0,0,0,.2);
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
  display: none;
  z-index:10000;
}
.close-btn:hover {
  color: var(--neutral-lt);
  background: var(--red-md);
  box-shadow: 0px 2px 4px rgba(0,0,0,.1);
}

/* REUSABLE TOGGLE CLASSES */
.hide {
  display: none;
}
.show {
  display: block;
}

/* FLOATING HEARTS */
.floating-hearts {
  position: absolute;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
}
.ri-heart-fill {
  font-size: 22px;
}
.hearts-row {
  display: flex;   
  justify-content: center;
  gap: 10px;
  width: 100%;
  opacity: 0;
}
.animated {
  animation-name: launch;
  animation-iteration-count: 1;
  animation-duration: 3s;
  animation-fill-mode: forwards;
}

@keyframes launch {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
.row-1 {
  color: var(--red-dk);
}
.row-2 {
  color: var(--red-md);
  animation-delay: 300ms;
}
.row-3 {
  color: var(--pink-dk);
  animation-delay: 600ms;
}
.row-4 {
  color: var(--purple-md);
   animation-delay: 900ms;
}
.row-5 {
  color: var(--purple-dk);
  animation-delay: 1200ms;
}
.row-6 {
  color: var(--purple-md);
  animation-delay: 1500ms;
  justify-content: flex-end;
  padding-right: 50px;
}
.row-7 {
  color: var(--pink-dk);
  animation-delay: 1800ms;  
  justify-content: flex-end;
  padding-right: 36px;
}
.row-8 {
  color: var(--red-md);
  animation-delay: 2100ms;
  justify-content: flex-end;
  padding-right: 20px;
}
.row-9 {
  color: var(--red-dk);
  animation-delay: 2400ms;
  justify-content: flex-end;
  padding-right: 10px;
}
.row-10 {
  color: var(--red-dk);
  animation-delay: 2400ms;
  justify-content: flex-end;
  padding-right: 20px;
