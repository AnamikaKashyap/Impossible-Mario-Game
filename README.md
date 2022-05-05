# Impossible-Mario-Game

https://anamikakashyap.github.io/Impossible-Mario-Game/

<!DOCTYPE html>

<html>

    <head>
 
       <title>Page Title</title>

<style>

@import url('https://fonts.googleapis.com/css2?family=Sriracha&family=Raleway&display=swap');

body {
    height: 100vh;
    background-color: white;
    overflow: hidden;
    user-select: none;
    font-family: Raleway;
}

button {
    outline: none;
}

#load {
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background-color: white;
    z-index: 1000000000000;
}

#loader {
    position: absolute;
    top: calc(50vh - 25px);
    left: 0;
    height: 50px;
    width: 100vw;
    text-align: center;
    font-size: 50px;
    font-weight: 900;
}

#yo {
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    overflow: hidden;
}

.controls {
    position: absolute;
    height: 69px;
    width: calc(50vw - 2px);
    text-align: center;
    background-color: rgba(150,150,150,0.4);
    display: none;
    top: calc(100vh - 70px);
    z-index: 100;
    border: 1px solid black;
    line-height: 70px;
    font-size: 30px;
    font-weight: 700;
    transition: 0.5s ease-out;
}

#show-hide-btn {
    position: absolute;
    top: 0;
    left: 10px;
    height: 30px;
    width: 180px;
    font-size: 18px;
    font-weight: 500;
    line-height: 30px;
    background: linear-gradient(0deg, rgb(144,238,144), rgb(250,150,200));
    z-index: 100;
    border-radius: 0 0 10px 10px;
    text-align: center;
}

#btn-left {
    left: 0;
}

#btn-right {
    left: 50vw;
}

#btn-up {
    top: calc(100vh - 140px);
    left: 25vw;
}

#shop-btn {
    position: absolute;
    top: 10px;
    left: 10px;
    height: 50px;
    width: 150px;
    background-color: rgb(255, 100, 100);
    border-radius: 10px;
    font-size: 25px;
    line-height: 50px;
    text-align: center;
    font-weight: 900;
}

#shop-btn:hover {
    background-color: rgb(255, 150, 150);
}

#shop {
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background-color: lightgreen;
    z-index: 500;
    display: none;
    overflow-y: scroll;
    overflow-x: hidden;
}

.shop-criteria {
    position: relative;
    left: 20px;
    margin-top: 30px;
    width: calc(100vw - 40px);
    border-radius: 10px;
    height: 180px;
    background-color: rgb(220, 150, 100);
}

.criteria {
    position: absolute;
    top: 20px;
    left: 0;
    width: 100%;
    text-align: center;
    font-weight: 900;
    font-size: 35px;
}

.bar {
    position: absolute;
    top: 100px;
    height: 20px;
    width: 80%;
    left: 10%;
    background-color: red;
    border-radius: 0 5px 5px 0;
}

#shop-heading {
    position: relative;
    top: 20px;
    left: 0;
    width: 100vw;
    font-size: 50px;
    text-align: center;
    font-weight: 900;
    letter-spacing: 5px;
}

.bar-complete {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    background-color: green;
    transition: width 1s;
}

.upgrade-btn {
    position: absolute;
    top: 130px;
    left: calc(100% - 210px);
    height: 50px;
    width: 200px;
    font-size: 20px;
    line-height: 50px;
    font-weight: 600;
    background-color: rgb(0,150,0);
    background-image: url("https://drive.google.com/thumbnail?id=1gZfMHuv4OBhtsiQ_91LQoHd74GhPdhCB");
    background-size: 50px 50px;
    background-position: 150px 0;
    background-repeat: no-repeat;
    border-radius: 0 0 5px 0;
    padding-left: 10px;
}

.upgrade-btn:hover {
    filter: brightness(120%);
}

#specials {
    position: relative;
    left: 0;
    margin-top: 50px;
    height: 80px;
    line-height: 80px;
    width: 100vw;
    text-align: center;
    font-size: 35px;
    font-weight: 900;
    background: linear-gradient(90deg, transparent, rgb(200,255,200), transparent);
}

.special-btn {
    position: relative;
    margin-top: 30px;
    left: 10px;
    height: 30px;
    width: 250px;
    font-size: 20px;
    font-weight: 900;
    background-color: rgb(0,150,0);
    background-image: url("https://drive.google.com/thumbnail?id=1gZfMHuv4OBhtsiQ_91LQoHd74GhPdhCB");
    background-size: 50px 50px;
    background-position: 215px 0;
    background-repeat: no-repeat;
    border-radius: 20px 0 20px 0;
    padding: 10px;
    line-height: 30px;
    animation: specialAnim 2s ease-in-out 0s infinite;
}

.special-cost {
    position: absolute;
    left: calc(100% - 80px);
    top: 10px;
}

#hard-game {
    width: 280px;
    font-size: 18px;
    font-weight: 600;
    background-position: 245px 0;
    height: 70px;
}

#not-rec {
    position: absolute;
    top: 50px;
    font-size: 15px;
    
}

@keyframes specialAnim {
    0%, 100% {filter: brightness(100%);}
    50% {filter: brightness(150%);}
}

#follow {
    position: relative;
    margin-top: 20px;
    left: 10px;
    height: 200px;
    width: calc(100vw - 20px);
    background-color: white;
    border-radius: 20px;
    transition: opacity 1s ease-in;
}

#plus100 {
    position: absolue;
    top: 50px;
    height: 100px;
    width: 100%;
    left: 0;
    color: black;
    font-weight: 900;
    font-size: 70px;
    text-align: center;
}

#follow-question {
    position: absolute;
    top: 20px;
    left: 0;
    height: 50px;
    width: 100%;
    text-align: center;
    font-size: 30px;
    line-height: 50px;
    background-color: rgba(255,255,200);
    border-radius: 20px;
    font-weight: 800;
}

.follow-answer {
    position: absolute;
    top: 120px;
    height: 50px;
    width: 100px;
    border-radius: 25px;
    text-align: center;
    font-size: 20px;
    line-height: 50px;
}

#follow-yes {
    left: calc(50% - 150px);
    background-color: green;
    animation: specialAnim 1s linear 0s infinite;
}

#follow-no {
    left: calc(50% + 50px);
    background-color: red;
}

#tutorials {
    position: relative;
    left: 0;
    margin-top: 60px;
    height: 80px;
    line-height: 80px;
    width: 100vw;
    text-align: center;
    font-size: 35px;
    font-weight: 900;
    background: linear-gradient(90deg, transparent, rgb(200,255,200), transparent);
}

#excuse {
    position: relative;
    margin-top: 5px;
    font-size: 15px;
    width: 100vw;
    left: 0;
    height: 50px;
}

.tut-lvl {
    position: relative;
    margin-top: 15px;
    left: 10px;
    width: calc(100vw - 20px);
    height: 300px;
    text-align: center;
    border-radius: 20px;
    background-color: rgba(255,255,255,0.2);
}

.tl-heading {
    position: absolute;
    top: 10px;
    left: 0;
    height: 50px;
    width: 100%;
    text-align: center;
    font-size: 35px;
    font-weight: 600;
}

video {
    width: 300px;
    position: absolute;
    top: 70px;
    left: calc(50% - 150px);
}

.cost {
    position: absolute;
    top: 0;
    left: calc(100% - 80px);
    font-weight: 900;
}

#shop-back {
    position: fixed;
    top: calc(100vh - 50px);
    left: calc(100vw - 100px);
    height: 50px;
    width: 100px;
    background-color: rgb(255,100,100);
    text-align: center;
    border-radius: 5px;
    font-size: 20px;
    line-height: 50px;
}

#notif {
    position: absolute;
    top: 20px;
    left: calc(50vw - 150px);
    height: 50px;
    width: 300px;
    background-color: white;
    border-radius: 10px;
    font-weight: 700;
    font-size: 20px;
    line-height: 50px;
    display: none;
    opacity: 0;
    transition: 0.5s ease-in-out;
    text-align: center;
    z-index: 1000;
}

#progress-bar {
    position: absolute;
    top: 100px;
    left: calc(50vw - 100px);
    width: 200px;
    height: 15px;
    border-radius: 10px;
    background: linear-gradient(0deg, pink, purple);
    z-index: 100;
    overflow: hidden;
}

#progress {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    background-color: lightblue;
}

#restart-btn {
    position: absolute;
    top: 35px;
    left: 15px;
    height: 30px;
    width: 150px;
    text-align: center;
    font-weight: 700;
    line-height: 30px;
    font-size: 20px;
    background-color: lightgreen;
    border-radius: 5px;
    z-index: 100;
}

#alert-background {
    display: none;
    z-index: 1000;
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background-color: rgba(0,0,0,0.5);
    opacity: 0;
    transition: 1s linear;
}

#alert {
    position: absolute;
    top: 100px;
    left: 50px;
    height: calc(100vh - 200px);
    width: calc(100vw - 100px);
    background-color: white;
    border-radius: 10px;
}

#alert-heading {
    position: absolute;
    top: 10px;
    left: 0;
    height: 30px;
    width: 100%;
    font-size: 30px;
    font-weight: 800;
    text-align: center;
}

#alert-text {
    position: absolute;
    top: 70px;
    left: 5%;
    width: 90%;
    font-size: 20px;
    height: calc(100vh - 200px - 150px - 70px - 10px);
    overflow-x: hidden;
}

#alert-illustration {
    position: absolute;
    top: calc(100% - 150px);
    left: calc(50% - 30px - 5px);
    height: 55px;
    width: 60px;
    border: 5px solid black;
    overflow: hidden;
}

#alert-button {
    position: absolute;
    top: calc(100% - 120px + 65px + 10px);
    height: 40px;
    width: 100px;
    left: calc(100% - 100px);
    background-color: rgb(100, 255, 100);
    font-size: 20px;
    line-height: 40px;
    text-align: center;
    border-radius: 10px 0 0 10px;
}

#alert-button:hover {
    background-color: rgb(150,255,150);
}

.ill {
    position: absolute;
    top: 5px;
    left: 5px;
    height: 50px;
    width: 50px;
    background-repeat: no-repeat;
}

#thorns {
    animation: thornAnim 3.2s linear 1s infinite;
}

#creature-ill {
    position: absolute;
    top: 0;
    left: 0;
    height: 50px;
    width: 50px;
    background-image: url("https://drive.google.com/thumbnail?id=1H0uQhROW_wF8Fbc5y03Pff4-0k5RB5a6");
    background-position: 0 0;
    background-size: 50px 50px;
    animation: creatureAnim 0.3s linear 1s infinite;
}

#cb-ill {
    position: absolute;
    top: 20px;
    left: 20px;
    height: 20px;
    width: 20px;
    background-image: url("https://drive.google.com/thumbnail?id=1voOdFQcPJlVRQSYIJwRXUpjmM317_A6F");
    background-size: 100% 100%;
    animation: cbAnim 2s linear 0s infinite;
}

@keyframes cbAnim {
    0%, 90% {left: 20px;}
    100% {left: -20px;}
}

#cannon-ill {
    position: absolute;
    top: 10px;
    left: 10px;
    height: 45px;
    width: 45px;
    background-image: url("https://drive.google.com/thumbnail?id=1P0G9swz7Qzp7e_8ZpiWHX2QWckDNwLr7");
    background-size: 100% 100%;
}

#ml-ill {
    position: absolute;
    top: 25px;
    left: 0;
    height: 10px;
    width: 20px;
    background-color: green;
    animation: mlAnim 2s linear 0s infinite;
}

@keyframes mlAnim {
    0%,100% {left: 0;}
    50% {left: 40px;}
}

@keyframes creatureAnim {
    0% {background-image: url("https://drive.google.com/thumbnail?id=19OPHBzr4qjak1Miu93FzFPMCyHqOyob4");}
    50% {background-image: url("https://drive.google.com/thumbnail?id=1H0uQhROW_wF8Fbc5y03Pff4-0k5RB5a6");}
}

@keyframes thornAnim {
    0% {background-position: 0 50px;}
    50% {background-position: 0 50px;}
    56.25% {background-position: 0 0;}
    100% {background-position: 0 0;}
}

#fake-land {
    left: 0;
    width: 60px;
    animation: fakeLandAnim 3.2s linear 1s infinite;
}

@keyframes fakeLandAnim {
    0% {top: 5px;}
    50% {top: 5px;}
    56.25% {top: 55px;}
    100% {top: 55px;}
}

#coins-count {
    position: absolute;
    left: 40px;
    width: 155px;
    height: 50px;
    top: 0;
    font-size: 15px;
    line-height: 25px;
    font-weight: 400;
}

#coins {
    position: absolute;
    top: 5px;
    left: calc(100vw - 180px);
    height: 25px;
    width: 180px;
    z-index: 100000;
    background-color: white;
    background-image: url("https://drive.google.com/thumbnail?id=1DiUmbfEi22zmfZw-ClXdJTbQ9eX45gfM");
    background-position: 10px 0;
    background-size: 20px 20px;
    background-repeat: no-repeat;
}

#plus-ten {
    position: absolute;
    height: 50px;
    width: 50px;
    display: none;
    opacity: 0;
    transition: 0.5s ease-in-out;
    z-index: 1000;
    font-weight: 700;
    font-size: 15px;
    text-align: center;
    line-height: 50px;
}

.game {
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background-color: white;
}

#dark {
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background-color: black;
    opacity: 0;
    transition: opacity 1s;
    z-index: 100;
}

.result {
    position: absolute;
    top: 100vh;
    left: 0;
    height: 100vh;
    width: 100vw;
    transition: 1s;
    z-index: 120;
}

.heading {
    position: absolute;
    top: 20vh;
    font-size: 60px;
    left: 0;
    width: 100vw;
    text-align: center;
    color: white;
}

.btn {
    position: absolute;
    top: 50vh;
    left: calc(50vw - 125px);
    width: 250px;
    text-align: center;
    font-size: 30px;
    height: 60px;
    line-height: 60px;
    color: white;
    background-color: green;
    border: none;
    border-radius: 20px;
}

.btn:hover {
    background-color: rgb(100, 255, 100);
}

.menu-btn {
    top: calc(50vh + 100px);
}

.next-lvl {
    top: calc(50vh + 200px);
}

#menu {
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    z-index: 1000;
    background-color: lightgreen;
    overflow-y: scroll;
}

.lvl {
    position: absolute;
    height: 130px;
    width: 100px;
    text-align: center;
    font-size: 20px;
    background-color: lightgray;
    background-image: url("https://drive.google.com/thumbnail?id=1i12uzb_yh6d2h2krRrc5rQRuNdpBPENb");
    background-size: 100px 100px;
    background-position-y: 30px;
    background-repeat: no-repeat;
    border-radius: 20px 20px 10px 10px;
}

#lvl-1 {
    top: 100px;
    left: 50px;
    background-image: url("https://drive.google.com/thumbnail?id=1PG4nGFDphbA7WTmnWq2jtKGatXm1sEf7");
}

#lvl-2 {
    top: 100px;
    left: 200px;
}

#lvl-3 {
    top: 300px;
    left: 50px;
}

#lvl-4 {
    top: 300px;
    left: 200px;
}

#lvl-5 {
    top: 500px;
    left: 50px;
}

.object {
    /transition: 0.2s linear;/
    position: absolute;
    z-index: 10;
}

.spikes {
    z-index: 5;
    background-image: url("https://drive.google.com/thumbnail?id=19gS3bZOh623rFMqVP2aeLsT6xAKJE7v4");
    background-size: 50px 50px;
    transition: top 0.2s linear;
}

.land {
    background-color: green;
}

.weak-land {
    background-color: green;
    transition: top 0.2s linear;
}

.box {
    background-image: url("https://drive.google.com/thumbnail?id=1qORyBsf4i4qA3g1jO1SlHz3rGmo4-nLX");
    background-size: 50px 50px;
}

.coin {
    background-image: url("https://drive.google.com/thumbnail?id=1DiUmbfEi22zmfZw-ClXdJTbQ9eX45gfM");
    background-size: 50px 50px;
    height: 50px;
    width: 50px;
}

.mario {
    position: absolute;
    top: 60vh;
    left: 20vw;
    background-image: url("https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4");
    height: 50px;
    width: 50px;
    background-size: contain;
    background-repeat: no-repeat;
    z-index: 1;
}

.creature {
    position: absolute;
    top: calc(60vh + 15px);
    height: 35px;
    width: 30px;
    background-image: url("https://drive.google.com/thumbnail?id=19OPHBzr4qjak1Miu93FzFPMCyHqOyob4");
    background-size: 40px 40px;
    background-position: -5px -5px;
    animation: creatureAnim 0.3s linear 1s infinite;
    /transition: .5s linear;/
}

@keyframes creatureAnim {
    0%,50% {background-image: url("https://drive.google.com/thumbnail?id=19OPHBzr4qjak1Miu93FzFPMCyHqOyob4");}
    51%,100% {background-image: url("https://drive.google.com/thumbnail?id=1H0uQhROW_wF8Fbc5y03Pff4-0k5RB5a6");}
}

.cannonball {
    position: absolute;
    top: calc(60vh + 15px);
    height: 20px;
    width: 20px;
    background-image: url("https://drive.google.com/thumbnail?id=1voOdFQcPJlVRQSYIJwRXUpjmM317_A6F");
    background-size: 100% 100%;
    z-index: 5;
}

.cannon {
    position: absolute;
    top: calc(60vh);
    height: 50px;
    width: 50px;
    background-image: url("https://drive.google.com/thumbnail?id=1P0G9swz7Qzp7e_8ZpiWHX2QWckDNwLr7");
    background-size: 100% 100%;
}

.moving-land {
    background-color: green;
}

#a {
    top: calc(60vh + 50px);
    left: 0;
    height: calc(40vh - 50px);
    width: 850px;
}

#b {
    top: calc(60vh);
    left: 700px;
    height: calc(50px);
    width: 100px;
}

#c {
    top: calc(60vh);
    left: 925px;
    height: calc(50px);
    width: 100px;
}

#d {
    left: 500px;
    top: calc(60vh - 50px);
    height: 100px;
    width: 50px;
}

#e {
    left: 600px;
    top: calc(60vh - 150px);
    height: 50px;
    width: 150px;
}

#f {
    left: 1100px;
    height: 50px;
    top: calc(60vh);
    width: 100px;
}

#g {
    left: 1300px;
    height: calc(40vh - 50px);
    top: calc(60vh + 50px);
    width: 300px;
}

#h {
    left: 800px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 100px;
}

#i {
    top: calc(60vh);
    left: 700px;
    height: calc(50px);
    width: 100px;
}

#j {
    top: calc(60vh - 150px);
    left: 700px;
    height: 50px;
    width: 50px;
}

#k {
    left: 1100px;
    height: 50px;
    top: calc(60vh);
    width: 50px;
}

#l {
    left: 1400px;
    top: calc(60vh - 50px);
}

.flag {
    position: absolute;
    background-image: url("https://drive.google.com/thumbnail?id=1XjUC1dzEP-GCM6KbyhShZjz1uFZv8TkF");
    background-size: 50px 50px;
    height: 50px;
    width: 50px;
    transition: top 0.5s linear;
    z-index: 20;
}

#m {
    left: 1400px;
    top: calc(60vh - 50px);
}

.stump {
    position: absolute;
    height: 100px;
    width: 5px;
    background-color: black;
    z-index: 20;
}

#n {
    left: 1400px;
    top: 0;
    height: calc(60vh + 50px);
    width: 50px;
}

#o {
    left: 500px;
    top: calc(60vh - 100px);
}

#p {
    left: 800px;
    top: calc(60vh);
}

#q {
    left: 850px;
    top: calc(60vh - 250px);
}

#r {
    left: 1150px;
    top: calc(60vh - 50px);
}

#aa {
    left: 0;
    height: calc(40vh - 50px);
    top: calc(60vh + 50px);
    width: 800px;
}

#ab {
    left: 400px;
    height: 50px;
    width: 50px;
    top: calc(60vh);
}

#ac {
    left: 450px;
    height: 100px;
    width: 50px;
    top: calc(60vh - 50px);
}

#ad {
    left: 500px;
    height: 150px;
    width: 50px;
    top: calc(60vh - 100px);
}

#ae {
    left: 550px;
    height: 200px;
    width: 50px;
    top: calc(60vh - 150px);
}

#af {
    left: 600px;
    height: 250px;
    width: 50px;
    top: calc(60vh - 200px);
}

#ag {
    left: 400px;
    top: calc(60vh);
    height: 50px;
    width: 50px;
}

#ah {
    left: 500px;
    top: calc(60vh - 100px);
    height: 50px;
    width: 50px;
}

#ai {
    left: 600px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 50px;
}

#aj {
    left: 700px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 200px;
}

#ak {
    left: 700px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 200px;
}

#al {
    left: 850px;
    height: calc(40vh - 50px);
    width: 100px;
    top: calc(60vh + 50px);
}

#am {
    left: 1000px;
    height: calc(40vh - 50px);
    width: 150px;
    top: calc(60vh + 50px);
}

#an {
    left: 1200px;
    height: calc(40vh - 50px);
    width: 50px;
    top: calc(60vh + 50px);
}

#ao {
    left: 950px;
    height: calc(40vh - 50px);
    top: calc(60vh + 50px);
    width: 50px;
}

#ap {
    left: 1150px;
    height: calc(40vh - 50px);
    top: calc(60vh + 50px);
    width: 50px;
}

#aq {
    left: 1350px;
    height: 50px;
    width: 50px;
    top: calc(60vh - 50px);
}

#ar {
    left: 1300px;
    height: 50px;
    width: 200px;
    top: calc(60vh - 50px);
}

#as {
    left: 1650px;
    height: calc(40vh - 50px);
    width: 200px;
    top: calc(60vh + 50px);
}

#at {
    left: 1700px;
    top: calc(60vh - 50px);
}

#au {
    left: 1700px;
    top: calc(60vh - 50px);
}

#av {
    left: 550px;
    top: calc(60vh - 200px);
}

#aw {
    left: 1050px;
    top: calc(60vh);
}

#ax {
    left: 1400px;
    top: calc(60vh - 100px);
}

#ay {
    left: 1000px;
    top: calc(60vh);
    height: 50px;
    width: 50px;
}

#az {
    left: 1000px;
    top: calc(60vh);
    height: 50px;
    width: 50px;
}

#ba {
    left: 1100px;
    top: calc(60vh - 150px);
    height: 50px;
    width: 150px;
}

#bb {
    left: 1150px;
    top: calc(60vh - 150px);
    height: 50px;
    width: 50px;
}

#bc {
    left: 1100px;
    top: calc(60vh - 200px);
}

#ca {
    left: 0;
    height: calc(40vh - 50px);
    top: calc(60vh + 50px);
    width: 450px;
}

#cb {
    left: 500px;
    height: 50px;
    width: 50px;
    top: calc(60vh);
}

#cc {
    left: 800px;
    height: 100px;
    width: 50px;
    top: calc(60vh - 50px);
}

#cd {
    left: 550px;
}

#ce {
    left: 500px;
    width: 50px;
    top: calc(60vh);
    height: 50px;
}

#cf {
    left: 450px;
    height: calc(40vh - 50px);
    top: calc(60vh + 50px);
    width: 50px;
}

#cg {
    left: 500px;
    height: calc(40vh - 50px);
    width: 500px;
    top: calc(60vh + 50px);
}

#ch {
    top: calc(60vh + 50px);
    left: 700px;
    height: 50px;
    width: 50px;
}

#ci {
    left: 900px;
    top: calc(60vh - 100px);
    height: 50px;
    width: 100px;
}

#cj {
    left: 1050px;
    top: calc(60vh + 50px);
    height: 50px;
    width: 50px;
}

#ck {
    left: 1250px;
    top: calc(60vh + 100px);
    height: 50px;
    width: 100px;
}

#cl {
    left: 1050px;
    top: calc(60vh);
}

#cm {
    left: 1400px;
    height: 50px;
    width: 50px;
    top: calc(60vh);
}

#cn {
    left: 1550px;
    height: 50px;
    width: 100px;
    top: calc(60vh + 100px);
}

#co {
    left: 1700px;
    height: 50px;
    width: 50px;
    top: calc(60vh);
}

#cp {
    left: 1700px;
    top: calc(60vh - 50px);
}

#cq {
    left: 1050px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 450px;
}

#cr {
    left: 1100px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 100px;
}

#cs {
    left: 1250px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 100px;
}

#ct {
    left: 1400px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 50px;
}

#cu {
    left: 1900px;
    top: calc(60vh + 50px);
    height: calc(40vh - 50px);
    width: 150px;
}

#cv {
    left: 2050px;
    top: calc(60vh - 50px);
    height: calc(40vh + 50px);
    width: 250px;
}

#cw {
    left: 2250px;
    top: calc(60vh - 150px);
    height: 100px;
    width: 50px;
}

#cx {
    left: 2100px;
    top: calc(60vh - 85px);
}

#cy {
    left: 2200px;
    height: 50px;
    width: 50px;
    top: calc(60vh - 50px);
}

#cz {
    left: 2500px;
    top: calc(60vh + 50px);
    height: calc(40vh - 50px);
    width: 200px;
}

#da {
    left: 2600px;
    top: calc(60vh - 50px);
}

#db {
    left: 2600px;
    top: calc(60vh - 50px);
}

#dc {
    left: 2000px;
    top: calc(60vh + 50px);
    height: 50px;
    width: 50px;
}

#dd {
    left: 2250px;
    top: calc(60vh - 200px);
}

#de {
    left: 1350px;
    top: calc(60vh - 250px);
}

#ea {
    left: 0;
    top: calc(60vh + 50px);
    height: calc(40vh - 50px);
    width: 600px;
}

#eb {
    left: 600px;
    width: 100px;
    height: calc(40vh);
    top: calc(60vh);
}

#ec {
    left: 700px;
    top: calc(60vh + 50px);
    width: 500px;
    height: calc(40vh - 50px);
}

#ed {
    left: 850px;
    top: calc(60vh - 60px);
    height: 50px;
    width: 100px;
}

#ee {
    left: 850px;
    top: calc(60vh - 60px);
    height: 50px;
    width: 100px;
}

#ef {
    left: 1170px;
}

#eg {
    left: 1150px;
}

#eh {
    left: 1300px;
    height: 50px;
    width: 100px;
    top: calc(60vh - 50px);
}

#ei {
    left: 1450px;
    height: 50px;
    width: 50px;
    top: calc(60vh - 150px);
}

#ej {
    left: 1350px;
    height: 50px;
    width: 50px;
    top: calc(60vh - 50px);
}

#ek {
    left: 1450px;
    height: 50px;
    width: 200px;
    top: calc(60vh + 50px);
}

#el {
    left: 1550px;
    height: 50px;
    width: 50px;
    top: calc(60vh + 50px);
}

#em {
    left: 1750px;
    height: 50px;
    width: 50px;
    top: calc(60vh);
}

#en {
    left: 1750px;
    top: calc(60vh - 50px);
}

#eo {
    left: 1850px;
    top: calc(60vh - 100px);
    height: 50px;
    width: 100px;
}

#ep {
    left: 1900px;
    top: calc(60vh - 100px);
    height: 50px;
    width: 50px;
}

#eq {
    left: 2000px;
    top: calc(60vh - 50px);
    height: 50px;
    width: 50px;
}

#er {
    left: 2150px;
    top: calc(60vh + 50px);
    height: 50px;
    width: 50px;
}

#es {
    left: 2250px;
    top: calc(60vh);
    height: calc(40vh);
    width: 250px;
}

#et {
    left: 2470px;
    top: calc(60vh - 35px);
}

#eu {
    left: 2450px;
    top: calc(60vh - 50px);
}

#ev {
    left: 2470px;
    top: calc(60vh - 85px);
}

#ew {
    left: 2450px;
    top: calc(60vh - 100px);
}

#ex {
    left: 2500px;
    top: calc(60vh - 150px);
    height: calc(40vh + 150px);
    width: 250px;
}

#ey {
    left: 2500px;
    top: calc(60vh - 185px);
}

#ez {
    left: 2750px;
    top: calc(60vh);
    height: calc(40vh);
    width: 200px;
}

#fa {
    left: 3100px;
    top: calc(60vh - 50px);
}

#fb {
    left: 3100px;
    top: calc(60vh - 50px);
}

#fc {
    left: 3050px;
    top: calc(60vh + 50px);
    width: 200px;
    height: calc(40vh - 50px);
}

#fd {
    left: 2450px;
    top: calc(60vh - 150px);
}

#fe {
    left: 2750px;
    top: calc(60vh - 50px);
}

#ff {
    left: 2150px;
    top: calc(60vh);
}

#ga {
    left: -50px;
    top: calc(60vh + 50px);
    height: calc(40vh - 50px);
    width: 850px;
}

#gb {
    left: -100px;
    top: calc(60vh);
    height: 50px;
    width: 100px;
}

#gc {
    left: -200px;
    top: calc(60vh - 50px);
    height: 50px;
    width: 100px;
}

#gd {
    left: -150px;
    top: calc(60vh - 160px);
    height: 50px;
    width: 50px;
}

#ge {
    left: -150px;
    top: calc(60vh - 210px);
}

#gf {
    left: 0;
    top: calc(60vh - 200px);
    height: 50px;
    width: 300px;
}

#gg {
    left: 450px;
    top: calc(60vh - 200px);
    height: 50px;
    width: 300px;
}

#gh {
    left: 450px;
    top: calc(60vh - 235px);
}

#gi {
    left: 400px;
    top: calc(60vh + 50px);
    height: 50px;
    width: 50px;
}

#gj {
    left: 750px;
    top: calc(60vh + 50px);
    height: 50px;
    width: 50px;
}

#gk {
    left: 900px;
    top: calc(60vh - 150px);
    height: 50px;
    width: 50px;
}

#gl {
    left: 800px;
    top: calc(60vh + 50px);
    height: calc(40vh - 50px);
    width: 150px;
}

#gm {
    left: 1100px;
    top: calc(60vh + 50px);
    height: 50px;
    width: 100px;
}

#gn {
    left: 1050px;
    top: -200px;
    height: 50px;
    width: 50px;
}

#go {
    left: 1500px;
    top: calc(60vh + 100px);
    height: calc(40vh - 100px);
    width: 100px;
}

#gp {
    left: 1750px;
    top: calc(60vh - 100px);
    height: calc(40vh + 100px);
    width: 250px;
}

#gq {
    left: 1750px;
    top: calc(60vh - 150px);
    height: 50px;
    width: 50px;
}

#gr {
    left: 1800px;
    top: calc(60vh - 100px);
    height: 50px;
    width: 50px;
}

#gs {
    left: 1650px;
    top: calc(60vh - 100px);
    height: 50px;
    width: 80px;
}

#gt {
    left: 1750px;
    top: calc(60vh - 200px);
}

#gu {
    left: 2570px;
    top: calc(60vh - 135px);
}

#gv {
    left: 2550px;
    top: calc(60vh - 150px);
}

#gw {
    left: 2500px;
    top: calc(60vh - 100px);
    height: 50px;
    width: 200px;
}

#gx {
    left: 2000px;
    top: calc(60vh + 50px);
    height: 50px;
    width: 300px;
}

#gy {
    left: 2650px;
    top: calc(60vh - 100px);
    height: 200px;
    width: 50px;
}

#gz {
    left: 2450px;
    top: calc(60vh + 50px);
    height: 50px;
    width: 250px;
}

#ha {
    left: 3300px;
    top: calc(60vh - 50px);
}

#hb {
    left: 3300px;
    top: calc(60vh - 50px);
}

#hc {
    left: 2250px;
    top: calc(60vh);
}

#hd {
    left: 2300px;
    top: calc(60vh + 170px);
    height: 50px;
    width: 100px;
}

#he {
    left: 2520px;
    top: calc(60vh + 15px);
}

#hf {
    left: 2500px;
    top: calc(60vh);
}

#hg {
    left: 3150px;
    top: calc(60vh + 150px);
    height: calc(40vh - 150px);
    width: 100px;
}

#hh {
    left: 3250px;
    top: calc(60vh + 50px);
    height: calc(40vh - 50px);
    width: 200px;
}

</style>

<script>

var coins = 0;
var mario,objects,keyspressed=[], t1=false, t2=false, t3=false, t4=false, t5=false, t6=false, t7=false, t8=false, t9=false, t10=false, height=0, jumpHeight=15, speed=5, maxJump=20, maxSpeed=8, contact=true,gravity=1, contact = [], currentAccel=0, lost = false, creatureSpeed=3, won = false, currentLevel = 0, levelsOpened = [0],clickedSHButton=0, lvlBonus=[20,25,30,40,50], cbSpeed=15;
var originalPosition = {};
let abcd = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','aa','ab','ac','ad','ae','af','ag','ah','ai','aj','ak','al','am','an','ao','ap','aq','ar','as','at','au','av','aw','ax','ay','az','ba','bb','bc','ca','cb','cc','cd','ce','cf','cg','ch','ci','cj','ck','cl','cm','cn','co','cp','cq','cr','cs','ct','cu','cv','cw','cx','cy','cz','da','db','dc','dd','de','ea','eb','ec','ed','ee','ef','eg','eh','ei','ej','ek','el','em','en','eo','ep','eq','er','es','et','eu','ev','ew','ex','ey','ez','fa','fb','fc','fd','fe','ff','ga','gb','gc','gd','ge','gf','gg','gh','gi','gj','gk','gl','gm','gn','go','gp','gq','gr','gs','gt','gu','gv','gw','gx','gy','gz','ha','hb','hc','hd','he','hf','hg','hh'];

var alertShown = {
    0: ["THE THORNS", "These are hidden, and can be anywhere (both on land as well as boxes), if mario steps on these, they will come up and you will lose.", "<div id = 'thorns' class = 'spikes ill'></div>", false],
    1: ["FAKE LAND", "The fake lands work similar to thorns, they can only be on land, they look same as normal land but as the mario steps on it, it goes down and mario falls.", "<div id = 'fake-land' class = 'land ill'></div>", false],
    2: ["CREATURES", "The creatures will walk around, they have some money in their bags(10), you can take away that money from them by jumping over them and they will vanish, but if you touched them on their side, they will take all your coins from your bag, and you will die, these might seem cute but they are very greedy. These creatures are not heavy enough to trigger traps.", "<div id = 'creature-ill'></div>", false],
    3: ["CANNON", "The cannon balls are very dangerous, they will take 5 coins from your bag if they hit you and you will die. You cannot defeat a cannon, you will have to dodge its shots.", "<div id = 'cb-ill'></div><div id = 'cannon-ill'></div>",false],
    4: ["MOVING LAND", "The moving land can never have traps. They will constantly move in their particular path. You will have to keep on moving at their speed in order not to fall from them.", "<div id = 'ml-ill'></div>",false],
}
var creatures = {
    "cd": [2, "cb", "cc", false],
    "cx": [2, "cu", "cw", false],
    "ey": [3, "es", "ez", false],
    "gh": [4, "gi", "gj", false],
}

var cannonballs = {
    "ef": [3,"eb","eg",false],
    "et": [3, "eq", "eu", false],
    "ev": [3, "ep", "ew", false],
    "gu": [4, "gq", "gv", false],
    "he": [4, "gp", "hf", false],
}
var movingLand = {
    "gm": [4, "gn", 200, 0, 5],
    "gs": [4, "gq", 0, 200, 3],
    "hd": [4, "gx", 700, 0, 5],
}

window.onload = function() {
    document.getElementById("load").style.display = "none";
    mario = document.getElementsByClassName("mario");
    objects = document.getElementsByClassName("object");
    for (let i of abcd) {
        let el = document.getElementById(i)
        originalPosition[i] = [el.offsetLeft+"px",el.offsetTop+"px"];
    }
    let i =1,el=document.getElementsByClassName("game");
    while (el[i]) {
        el[i].style.display = "none";
        i++;
    }
    Alert("SHOP", "Welcome to the game 'MARIO'! Here there are 5 levels that you have to complete, you can control the mario by using the buttons on the screen ONLY for mobiles or the keys on your keyboard (ArrowLeft-to move left, ArrowRight-to move right, ArrowUp-to jump). Laptops/PC are recommended to play this game, as the area of vision increases a lot and also the controls are easier to handle. There are different types of obstacles that will come in your way, you might have to try the same level many times to know about all the trap placements. Please don't get furstrated playing this game, actually the real game is known to make players mad xD. You will have to have some patience to finish the game. The shop is a very important part of the game, you will have to keep upgrading your mario in order to complete higher levels easily, for that you will have to collect coins kept on your path, each coin has a value of 5 in the first level and it will subsequently increase by 5 in the next levels, you get huge coin bonuses when you complete levels. You can unlock all the levels in just 10 coisn from the market. In order to see how to complete the levels there videos also at the bottom of the shop. By the way, all the images seen in this game are drawn by me!", "");
    document.getElementById("btn-left").addEventListener("touchstart", function() {
        if (!lost && !won && !t1) {
            t1 = setInterval(MoveLeft, 25);
        }
    });
    document.getElementById("btn-right").addEventListener("touchstart", function() {
        if (!lost && !won && !t2) {
            t2 = setInterval(MoveRight, 25);
        }
    });
    document.getElementById("btn-up").addEventListener("touchstart", function() {
        if (!lost && !won && checkContact().includes("down")) {
            MoveUp();
        }
    });
    document.getElementById("btn-left").addEventListener("touchend", function() {
        mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
        clearInterval(t4);
        t4 = false;
        clearInterval(t1);
        t1 = false;
    });
    document.getElementById("btn-right").addEventListener("touchend", function() {
        mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
        clearInterval(t4);
        t4 = false;
        clearInterval(t2);
        t2 = false;
    });
};

function CannonBallMovement() {
    for (let i of Object.keys(cannonballs)) {
        if (cannonballs[i][0] === currentLevel) {
            let el = document.getElementById(i), el2=document.getElementById(cannonballs[i][1]);
            if (el.offsetLeft >= el2.offsetLeft+el2.offsetWidth-Math.ceil(cbSpeed/2)-40 && el.offsetLeft <= el2.offsetLeft+el2.offsetWidth+Math.ceil(cbSpeed/2)-40) {
                el.style.left = document.getElementById(cannonballs[i][2]).offsetLeft+20+"px";
                cannonballs[i][3]=true;
                setTimeout(function() {cannonballs[i][3]=false;},1000);
            }
            else {
                if (!cannonballs[i][3]) {
                    el.style.left = el.offsetLeft-cbSpeed + "px";
                }
            }
        }
    }
}

function LandMovement() {
    for (let i of Object.keys(movingLand).filter((x)=>movingLand[x][0]==currentLevel)) {
        //document.write("hello");
        let el=document.getElementById(i),el2=document.getElementById(movingLand[i][1]);
        if (movingLand[i][2]!=0) {
            if (el.offsetLeft<=el2.offsetLeft+el2.offsetWidth) {
                movingLand[i][4] = Math.abs(movingLand[i][4]);
            }
            if (el.offsetLeft>=el2.offsetLeft+el2.offsetWidth+movingLand[i][2]) {
                movingLand[i][4] = -Math.abs(movingLand[i][4]);
            }
            el.style.left = el.offsetLeft+movingLand[i][4]+"px";
        }
        else {
            if (el.offsetTop<=el2.offsetTop+el2.offsetHeight) {
                movingLand[i][4] = Math.abs(movingLand[i][4]);
            }
            if (el.offsetTop>=el2.offsetTop+el2.offsetHeight+movingLand[i][3]) {
                movingLand[i][4] = -Math.abs(movingLand[i][4]);
            }
            el.style.top = el.offsetTop+movingLand[i][4]+"px";
        }
    }
}

function HardGame() {
    if (coins>=50) {
        coins-=50;
        Notif("All thorns disclosed.");
        let i = 0, el=document.getElementsByClassName("spikes");
        while (el[i]) {
            el[i].style.zIndex = "50";
            i++;
        }
        document.getElementById("hard-game").style.display = "none";
    }
    else {
        Notif("Not enough money");
    }
}

function FollowYes() {
    let el = document.getElementById("follow");
    el.style.backgroundColor = "transparent";
    el.innerHTML = "<div id='plus100'>+100</div>";
    el.style.opacity = "0";
    coins+=100;
    setTimeout(function() {
        el.style.display = "none";
    }, 1000)
}

function FollowNo() {
    document.getElementById("follow").style.display = "none";
}

function restartLevel() {
    OpenLevel(currentLevel);
}

function CreaturesMovement() {
    let x = Object.keys(creatures);
    for (let i of x) {
        if (creatures[i][0] == currentLevel) {
            let el = document.getElementById(i),el2=document.getElementById(creatures[i][1]),el3=document.getElementById(creatures[i][2]);
            if (el.offsetLeft >= el2.offsetLeft+el2.offsetWidth-Math.ceil(creatureSpeed/2) && el.offsetLeft <= el2.offsetLeft+el2.offsetWidth+Math.ceil(creatureSpeed/2)) {
                el.style.transform = "none";
            }
            else if (el.offsetLeft >= el3.offsetLeft-Math.ceil(creatureSpeed/2)-30 && el.offsetLeft <= el3.offsetLeft+Math.ceil(creatureSpeed/2)-30) {
                el.style.transform = "rotateY(180deg)";
            }
            if (el.style.transform != "rotateY(180deg)") {
                el.style.left = el.offsetLeft+creatureSpeed+"px";
            }
            else {
                el.style.left = el.offsetLeft-creatureSpeed+"px";
            }
        }
    }
}

function Alert(heading, text, illustration) {
    document.getElementById("alert-background").style.display = "block";
    document.getElementById("alert-background").style.opacity = "1";
    document.getElementById("alert-heading").innerHTML = heading;
    document.getElementById("alert-text").innerHTML = text;
    if (illustration != "") {
        document.getElementById("alert-illustration").innerHTML = illustration;
        document.getElementById("alert-illustration").style.display = "block";
        document.getElementById("alert-text").style.height = "calc(100vh - 200px - 150px - 70px - 10px)";
    }
    else {
        document.getElementById("alert-illustration").style.display = "none";
        document.getElementById("alert-text").style.height = "calc(100vh - 200px - 150px)";
    }
}

const Close = () => {
    document.getElementById("alert-background").style.display = "none";
    document.getElementById("alert-background").style.opacity = "0";
}

setInterval(function() {
    document.getElementById("coins-count").innerHTML = `Coin balance:  ${coins}`;
}, 200);

function OpenShop() {
    document.getElementById("menu").style.display = "none";
    document.getElementById("shop").style.display = "block";
    document.getElementById("speed-bar").style.width = speed/maxSpeed*100+"%";
    document.getElementById("jump-bar").style.width = jumpHeight/maxJump*100+"%";
}

function CloseShop() {
    document.getElementById("menu").style.display = "block";
    document.getElementById("shop").style.display = "none";
}

function ShowHideButton() {
    clickedSHButton++;
    if (clickedSHButton%2) {
        document.getElementById("show-hide-btn").innerHTML = "SHOW BUTTONS";
        for (let i = 0; i < 3; i++) {
            document.getElementsByClassName("controls")[i].style.top = "100vh";
        }
    }
    else {
        document.getElementById("show-hide-btn").innerHTML = "HIDE BUTTONS";
        for (let i = 0; i < 3; i++) {
            if (i<2) {
                document.getElementsByClassName("controls")[i].style.top = "calc(100vh - 70px)";
            }
            else {
                document.getElementsByClassName("controls")[i].style.top = "calc(100vh - 140px)";
            }
        }
    }
}

function UnlockLevels() {
    if (coins >= 10) {
        coins-=10
        Notif("All levels unlocked!")
        document.getElementById("shop-unlock").style.display = "none";
        levelsOpened = [0,1,2,3,4];
        for (let i = 0; i < 5; i++) {
            let lvl = document.getElementsByClassName("lvl")[i];
            if (lvl.style.backgroundImage == 'url("https://drive.google.com/thumbnail?id=1i12uzb_yh6d2h2krRrc5rQRuNdpBPENb")') {
                lvl.style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1PG4nGFDphbA7WTmnWq2jtKGatXm1sEf7')";
            }
        }
    }
    else {
        Notif("Not enough money.");
    }
}

function speedInc() {
    let cost = document.getElementById("speed-inc-cost");
    if (cost.innerHTML <= coins && speed < maxSpeed) {
        coins-=cost.innerHTML;
        cost.innerHTML*=2;
        speed+=0.5;
        document.getElementById("speed-bar").style.width = speed/maxSpeed*100+"%";
    }
    else if (cost.innerHTML > coins) {
        Notif("Not enough money.")
    }
    else {
        Notif("max level reached.")
    }
}

function Progress() {
    let el = document.getElementsByClassName("flag")[currentLevel];
    let progress = (parseInt(originalPosition[el.id][0])-el.offsetLeft+50)/(parseInt(originalPosition[el.id][0])-document.getElementsByTagName("body")[0].offsetWidth*0.3)*100;
    document.getElementById("progress").style.width = progress+"%";
}

function jumpInc() {
    let cost = document.getElementById("jump-inc-cost");
    if (cost.innerHTML <= coins && jumpHeight < maxJump) {
        coins-=cost.innerHTML;
        cost.innerHTML=+cost.innerHTML+30;
        jumpHeight+=0.5;
        document.getElementById("jump-bar").style.width = jumpHeight/maxJump*100+"%";
    }
    else if (cost.innerHTML > coins) {
        Notif("Not enough money.")
    }
    else {
        Notif("Max level reached.")
    }
}

function Notif(a) {
    let n = document.getElementById("notif");
    n.innerHTML = a;
    n.style.display = "block";
    n.style.opacity = "1";
    setTimeout(function() {
        setTimeout(function() {
            n.style.display = "none";
        },500);
        n.style.opacity = "0";
    },2000)
}

function OpenLevel(x) {
    if (levelsOpened.includes(x)) {
        currentLevel = x;
        document.getElementById("menu").style.display = "none";
        let game = document.getElementsByClassName("game"), i = 0;
        while (game[i]) {
            game[i].style.display = "none";
            i++;
        }
        game[currentLevel].style.display = "block";
        document.getElementById("lost").style.top = "100vh";
        document.getElementById("won").style.top = "100vh";
        document.getElementById("dark").style.opacity = "0";
        lost = false;
        won = false;
        returnToOriginalPosition();
        if (!t5) {
            t5 = setInterval(Gravity, 25);
        }
        if (!t3) { 
            t3 = setInterval(AfterLost, 500);
        }
        if (!t6) {
            t6 = setInterval(AfterWon, 500);
        }
        if (!t7) {
            t7 = setInterval(Progress, 100);
        }
        if (!t8) {
            t8 = setInterval(CreaturesMovement, 50);
        }
        if (!t9) {
            t9 = setInterval(CannonBallMovement, 40);
        }
        if (!t10) {
            t10 = setInterval(LandMovement, 50);
        }
        mario[currentLevel].style.top = "60vh";
        if (alertShown[currentLevel][3] == false) {
            let x = alertShown[currentLevel];
            Alert(...x.slice(0,3));
            alertShown[currentLevel][3] = true;
        }
        for (let i = 0; i < 3; i++) {
            document.getElementsByClassName("controls")[i].style.display = "block";
        }
        document.getElementById("show-hide-btn").style.display = "block";
    }
}

function NextLevel() {
    currentLevel++;
    OpenLevel(currentLevel);
}

function ShowMenu() {
    document.getElementsByClassName("lvl")[Math.max(...levelsOpened)].style.backgroundImage = 'url("https://drive.google.com/thumbnail?id=1PG4nGFDphbA7WTmnWq2jtKGatXm1sEf7")';
    document.getElementById("menu").style.display = "block";
    for (let i = 0; i < 3; i++) {
        document.getElementsByClassName("controls")[i].style.display = "none";
    }
    document.getElementById("show-hide-btn").style.display = "none";
    clearInterval(t7);
    t7 = false;
    clearInterval(t8);
    t8 = false;
    clearInterval(t9);
    t9 = false;
    clearInterval(t10);
    t10 = false;
}

function AfterLost() {
    if (mario[currentLevel].offsetTop >= document.getElementsByTagName("body")[0].offsetHeight) {
        clearInterval(t5);
        t5 = false;
        document.getElementById("lost").style.top = "0";
        document.getElementById("dark").style.opacity = "0.7";
        clearInterval(t3);
        t3 = false;
        clearInterval(t6);
        t6 = false;
    }
}

function AfterWon() {
    if (document.getElementsByClassName("flag")[currentLevel].offsetTop == Math.round(document.getElementsByTagName("body")[0].offsetHeight*0.6)) {
        clearInterval(t5);
        t5 = false;
        document.getElementById("won").style.top = "0";
        document.getElementsByClassName("next-lvl")[0].style.display = "block";
        document.getElementById("dark").style.opacity = "0.7";
        clearInterval(t3);
        t3 = false;
        clearInterval(t6);
        t6 = false;
        if (currentLevel != 4) {
            levelsOpened.push(currentLevel+1);
        }
        else {
            document.getElementsByClassName("next-lvl")[0].style.display = "none";
            document.getElementsByClassName("lvl")[currentLevel].style.backgroundImage = 'url("https://drive.google.com/thumbnail?id=1fAyA76nBef2L3I1F-CA4HxWyIVxNr1TH")';
        }
        document.getElementsByClassName("lvl")[currentLevel].style.backgroundImage = 'url("https://drive.google.com/thumbnail?id=1fAyA76nBef2L3I1F-CA4HxWyIVxNr1TH")';
        coins+=lvlBonus[currentLevel];
        lvlBonus[currentLevel] = 0;
    }
}

function Replay() {
    document.getElementById("lost").style.top = "100vh";
    document.getElementById("won").style.top = "100vh";
    document.getElementById("dark").style.opacity = "0";
    document.getElementsByClassName("flag")[currentLevel].style.top = "calc(60vh - 50px)";
    lost = false;
    won = false;
    returnToOriginalPosition();
    setTimeout(function() {
        t5 = setInterval(Gravity, 25);
        t3 = setInterval(AfterLost, 500);
        t6 = setInterval(AfterWon, 500);
        mario[currentLevel].style.top = "60vh";
    }, 1000);
}

function returnToOriginalPosition() {
    let keys = Object.keys(originalPosition), values = Object.values(originalPosition);
    for (let i=0; i < keys.length; i++) {
        document.getElementById(keys[i]).style.left = values[i][0];
        document.getElementById(keys[i]).style.top = values[i][1];
    }
}

window.addEventListener("keydown", function(e) {
    keyspressed.push(e.key);
    if (!lost && !won && keyspressed.includes("ArrowLeft") && !t1) {
        t1 = setInterval(MoveLeft, 25);
    }
    if (!lost && !won && keyspressed.includes("ArrowRight") && !t2) {
        t2 = setInterval(MoveRight, 25);
    }
    if (!lost && !won && keyspressed.includes("ArrowUp") && checkContact().includes("down")) {
        MoveUp()
    }
    keyspressed.splice(keyspressed.indexOf(e.key), 1);
});

window.addEventListener("keyup", function(e) {
    if (e.key != "ArrowUp") {
        mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
        clearInterval(t4);
        t4 = false;
    }
    if (e.key == "ArrowLeft") {
        clearInterval(t1);
        t1 = false;
    }
    if (e.key == "ArrowRight") {
        clearInterval(t2);
        t2 = false;
    }
});

function CoinTouched(x,y,z=5+5*currentLevel) {
    var plusTen = document.getElementById("plus-ten");
    plusTen.style.left = x;
    plusTen.style.top = y;
    plusTen.innerHTML = "+"+z;
    plusTen.style.display = "block";
    plusTen.style.opacity = "1";
    setTimeout(function() {
        plusTen.style.top = plusTen.offsetTop-50 + "px";
        plusTen.style.opacity = "0";
        setTimeout(function() {plusTen.style.display = "none";},500);
    }, 500)
}

function checkContact() {
    let i = 0;
    contact = [];
    while (objects[i]) {
        if (document.getElementsByClassName("game")[currentLevel].contains(objects[i])) {
            if (!lost && mario[currentLevel].offsetTop >= objects[i].offsetTop-51-currentAccel/2-(objects[i].classList.contains("up-down") ? 3 : 0) && mario[currentLevel].offsetTop <= objects[i].offsetTop-49+currentAccel/2+(objects[i].classList.contains("up-down") ? 3 : 0) && mario[currentLevel].offsetLeft > objects[i].offsetLeft-35 && mario[currentLevel].offsetLeft < objects[i].offsetLeft+objects[i].offsetWidth-15 && currentAccel >= 0) {
                if (objects[i].classList.contains("coin")) {
                    CoinTouched(objects[i].offsetLeft+"px", objects[i].offsetTop+"px");
                    coins+=5+5*currentLevel;
                    objects[i].style.top = "-50px";
                    objects[i].style.left = "0";
                    originalPosition[objects[i].id] = ["0", "-50px"];
                }
                else if (objects[i].classList.contains("creature")) {
                    if (!creatures[objects[i].id][3]) {
                        coins+=10;
                        CoinTouched(objects[i].offsetLeft+"px", objects[i].offsetTop+"px", 10);
                        creatures[objects[i].id][3] = true;
                    }
                    objects[i].style.top = "-50px";
                    objects[i].style.left = "0";
                }
                else if (objects[i].classList.contains("cannonball")) {
                    if (coins>=5) {coins-=5;}
                    currentAccel = -jumpHeight;
                    mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
                    mario[currentLevel].style.top = objects[i].offsetTop-50+currentAccel+"px";
                    clearInterval(t1);
                    clearInterval(t2);
                    clearInterval(t4);
                    t1 = t2 = t4 = false;
                    lost = true;
                }
                else {
                    contact.push("down");
                    mario[currentLevel].style.top = objects[i].offsetTop-50+"px";
                    if (objects[i].classList.contains("spikes")) {
                        currentAccel = -jumpHeight;
                        mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
                        mario[currentLevel].style.top = objects[i].offsetTop-50+currentAccel+"px";
                        objects[i].style.top = objects[i].offsetTop-50+"px";
                        clearInterval(t1);
                        clearInterval(t2);
                        clearInterval(t4);
                        t1 = t2 = t4 = false;
                        lost = true;
                    }
                    if (objects[i].classList.contains("weak-land")) {
                        mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
                        objects[i].style.top = "100vh";
                        clearInterval(t1);
                        clearInterval(t2);
                        clearInterval(t4);
                        t1 = t2 = t4 = false;
                        lost = true;
                    }
                }
            }
            if (!lost && !won && mario[currentLevel].offsetTop >= objects[i].offsetTop+objects[i].offsetHeight+currentAccel/2 && mario[currentLevel].offsetTop <= objects[i].offsetTop+objects[i].offsetHeight-currentAccel/2 && mario[currentLevel].offsetLeft > objects[i].offsetLeft-35 && mario[currentLevel].offsetLeft < objects[i].offsetLeft+objects[i].offsetWidth-15 && currentAccel <= 0) {
                if (objects[i].classList.contains("coin")) {
                    coins+=5+5*currentLevel;
                    CoinTouched(objects[i].offsetLeft+"px", objects[i].offsetTop+"px");
                    objects[i].style.top = "-50px";
                    objects[i].style.left = "0";
                    originalPosition[objects[i].id] = ["0", "-50px"];
                }
                else {
                    contact.push("up");
                    mario[currentLevel].style.top = objects[i].offsetTop+objects[i].offsetHeight+1+"px";
                    currentAccel = 0;
                }   
            }
            if (!lost && !won && Object.values(cannonballs).map((x)=>x[0]).includes(currentLevel)) {
                for (let i of Object.keys(cannonballs).filter((x)=>cannonballs[x][0]==currentLevel)) {
                    let el = document.getElementById(i);
                    if (mario[currentLevel].offsetLeft >= el.offsetLeft-50 && mario[currentLevel].offsetLeft <= el.offsetLeft-20 && mario[currentLevel].offsetTop >= el.offsetTop-30 && mario[currentLevel].offsetTop <= el.offsetTop+30) {
                        if (coins>=5) {coins-=5;}
                        currentAccel = -jumpHeight;
                        mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
                        mario[currentLevel].style.top = objects[i].offsetTop-50+currentAccel+"px";
                        clearInterval(t1);
                        clearInterval(t2);
                        clearInterval(t4);
                        t1 = t2 = t4 = false;
                        lost = true;
                    }
                }
            }
            if (!lost && !won && mario[currentLevel].offsetLeft >= objects[i].offsetLeft-35-Math.ceil(speed/2) && mario[currentLevel].offsetLeft <= objects[i].offsetLeft-35+Math.ceil(speed/2) && mario[currentLevel].offsetTop >= objects[i].offsetTop-49+currentAccel/2 && mario[currentLevel].offsetTop <= objects[i].offsetTop+objects[i].offsetHeight-1-currentAccel/2) {
                if (objects[i].classList.contains("coin")) {
                    coins+=5+5*currentLevel;
                    CoinTouched(objects[i].offsetLeft+"px", objects[i].offsetTop+"px");
                    objects[i].style.top = "-50px";
                    objects[i].style.left = "0";
                    originalPosition[objects[i].id] = ["0", "-50px"];
                }
                else if (objects[i].classList.contains("creature")) {
                    coins = 0;
                    currentAccel = -jumpHeight;
                    mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
                    mario[currentLevel].style.top = mario.offsetTop+currentAccel+"px";
                    clearInterval(t1);
                    clearInterval(t2);
                    clearInterval(t4);
                    t1 = t2 = t4 = false;
                    lost = true;
                }
                else {                
                    mario[currentLevel].style.left = objects[i].offsetLeft-35+"px";
                    contact.push("right");
                    if (objects[i].classList.contains("end")) {
                        mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
                        mario[currentLevel].style.top = "calc(60vh)";
                        setTimeout(function() {
                            mario[currentLevel].style.top = "calc(60vh)";
                        }, 50);
                        clearInterval(t5);
                        t5 = false;
                        document.getElementsByClassName("flag")[currentLevel].style.top = "calc(60vh)";
                        won = true;
                        clearInterval(t1);
                        clearInterval(t2);
                        clearInterval(t4);
                        t1 = t2 = t4 = false;
                    }
                }
            }
            if (!lost && !won && mario[currentLevel].offsetLeft >= objects[i].offsetLeft+objects[i].offsetWidth-15-Math.ceil(speed/2) && mario[currentLevel].offsetLeft <= objects[i].offsetLeft+objects[i].offsetWidth-15+Math.ceil(speed/2) && mario[currentLevel].offsetTop >= objects[i].offsetTop-49+currentAccel/2 && mario[currentLevel].offsetTop <= objects[i].offsetTop+objects[i].offsetHeight-1-currentAccel/2) {
                if (objects[i].classList.contains("coin")) {
                    coins+=5+5*currentLevel;
                    CoinTouched(objects[i].offsetLeft+"px", objects[i].offsetTop+"px");
                    objects[i].style.top = "-50px";
                    objects[i].style.left = "0";
                    originalPosition[objects[i].id] = ["0", "-50px"];
                }
                else if (objects[i].classList.contains("creature")) {
                    coins=0;
                    currentAccel = -jumpHeight;
                    mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
                    mario[currentLevel].style.top = mario.offsetTop+currentAccel+"px";
                    clearInterval(t1);
                    clearInterval(t2);
                    clearInterval(t4);
                    t1 = t2 = t4 = false;
                    lost = true;
                }
                else {
                    mario[currentLevel].style.left = objects[i].offsetLeft+objects[i].offsetWidth-15+"px";
                    contact.push("left");
                }
            }
        }
        i++;
    }
    return contact;
}

function MoveLeft() {
    mario[currentLevel].style.transform = "rotateY(180deg)";
    if (!t4) {
        t4 = setInterval(Walk, 200);
        mario[currentLevel].style.backgroundImage = "url('https://i.ibb.co/NnZ6LWj/mario.png')";
        setTimeout(function() {
            mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
        }, 100);
    }
    if (!checkContact().includes("left")) {
        let i = 0;
        while (objects[i]) {
            objects[i].style.left = `${objects[i].offsetLeft+speed}px`;
            i++;
        }
    }
}

function MoveRight() {
    mario[currentLevel].style.transform = "none";
    if (!t4) {
        mario[currentLevel].style.backgroundImage = "url('https://i.ibb.co/NnZ6LWj/mario.png')";
        setTimeout(function() {
            mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
        }, 100);
        t4 = setInterval(Walk, 200);
    }
    if (!checkContact().includes("right")) {
        let i = 0;
        while (objects[i]) {
            objects[i].style.left = `${objects[i].offsetLeft-speed}px`;
            i++;
        }
    }
}

function MoveUp() {
    mario[currentLevel].style.top = `${mario[currentLevel].offsetTop-jumpHeight}px`;
    currentAccel = -jumpHeight;
}

function Gravity() {
    if (!checkContact().includes("down") || lost) {
        currentAccel+=gravity;
        mario[currentLevel].style.top = mario[currentLevel].offsetTop+currentAccel+"px";
    }
    else {
        currentAccel = 0;
    }
}

function Walk() {
    mario[currentLevel].style.backgroundImage = "url('https://i.ibb.co/NnZ6LWj/mario.png')";
    setTimeout(function() {
        mario[currentLevel].style.backgroundImage = "url('https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4')";
    }, 100)
}


</script>

    </head>

    <body>
  
      <div id = "load">
<div id = "loader">LOADING...</div>
</div>

        <div id = "yo">
     
   <img src = "https://i.ibb.co/NnZ6LWj/mario.png" style = "display: block;">

        <img src = "https://drive.google.com/thumbnail?id=1XjUC1dzEP-GCM6KbyhShZjz1uFZv8TkF" style = "display: none;">
 
       <img src = "https://drive.google.com/thumbnail?id=1Y2USixLoQlYpEHiONc3vTJfLcP5UZMV4" style = "display: none;">
      
  <img src = "https://drive.google.com/thumbnail?id=1qORyBsf4i4qA3g1jO1SlHz3rGmo4-nLX" style = "display: none;">
  
      <img src = "https://drive.google.com/thumbnail?id=19gS3bZOh623rFMqVP2aeLsT6xAKJE7v4" style = "display: none;">
      
  <img src = "https://drive.google.com/thumbnail?id=1i12uzb_yh6d2h2krRrc5rQRuNdpBPENb" style = "display: none;">
   
     <img src = "https://drive.google.com/thumbnail?id=1DiUmbfEi22zmfZw-ClXdJTbQ9eX45gfM" style = "display: none;">
      
  <img src = "https://drive.google.com/thumbnail?id=1fAyA76nBef2L3I1F-CA4HxWyIVxNr1TH" style = "display: none;">
   
     <img src = "https://drive.google.com/thumbnail?id=1PG4nGFDphbA7WTmnWq2jtKGatXm1sEf7" style = "display: none;">
      
  <img src = "https://drive.google.com/thumbnail?id=1gZfMHuv4OBhtsiQ_91LQoHd74GhPdhCB" style = "display: none;">
   
     <img src = "https://drive.google.com/thumbnail?id=1H0uQhROW_wF8Fbc5y03Pff4-0k5RB5a6" style = "display: none;">
  
      <img src = "https://drive.google.com/thumbnail?id=19OPHBzr4qjak1Miu93FzFPMCyHqOyob4" style = "display: none;">
 
       <img src = "https://drive.google.com/thumbnail?id=1P0G9swz7Qzp7e_8ZpiWHX2QWckDNwLr7" style = "display: none;">
   
     <img src  "https://drive.google.com/thumbnail?id=1voOdFQcPJlVRQSYIJwRXUpjmM317_A6F" style = "display: none;">    
  
      <div id = "menu">
          
  <div id = "shop-btn" onclick = "OpenShop();">SHOP</div>
    
        <div id = "lvl-1" class = "lvl" onclick = "OpenLevel(0)" style = 'background-image: url("https://drive.google.com/thumbnail?id=1PG4nGFDphbA7WTmnWq2jtKGatXm1sEf7");'>LEVEL 1</div>
         
   <div id = "lvl-2" class = "lvl" onclick = "OpenLevel(1)" style = 'background-image: url("https://drive.google.com/thumbnail?id=1i12uzb_yh6d2h2krRrc5rQRuNdpBPENb");'>LEVEL 2</div>
    
        <div id = "lvl-3" class = "lvl" onclick = "OpenLevel(2)" style = 'background-image: url("https://drive.google.com/thumbnail?id=1i12uzb_yh6d2h2krRrc5rQRuNdpBPENb");'>LEVEL 3</div>
      
      <div id = "lvl-4" class = "lvl" onclick = "OpenLevel(3)" style = 'background-image: url("https://drive.google.com/thumbnail?id=1i12uzb_yh6d2h2krRrc5rQRuNdpBPENb");'>LEVEL 4</div>
     
       <div id = "lvl-5" class = "lvl" onclick = "OpenLevel(4)" style = 'background-image: url("https://drive.google.com/thumbnail?id=1i12uzb_yh6d2h2krRrc5rQRuNdpBPENb");'>LEVEL 5</div>
   
     </div>
        <div id = "shop">
    
        <div id = "shop-heading">SHOP</div>
     
       <div id = "shop-speed" class = "shop-criteria">

                <div class = "criteria">SPEED</div>
  
              <div class = "bar">
      
              <div id = "speed-bar" class = "bar-complete"></div>
      
          </div>
  
              <div class = "upgrade-btn" onclick = "speedInc()">
    
                UPGRADE
       
             <div id = "speed-inc-cost" class="cost">20</div>
      
          </div>
    
        </div>
      
      <div id = "shop-jump" class = "shop-criteria">
     
           <div class = "criteria">JUMP</div>
          
      <div class = "bar">
    
                <div id = "jump-bar" class = "bar-complete"></div>
    
            </div>
  
              <div class = "upgrade-btn" onclick="jumpInc()">
      
              UPGRADE
     
               <div id = "jump-inc-cost" class="cost">10</div>
        
        </div>
  
          </div>
  
          <div id = "specials">SPECIALS</div>
   
         <div id = "shop-unlock" class = "special-btn" onclick = "UnlockLevels()">Unlock all levels: <div class = "special-cost">10</div></div>
  
          <div id = "hard-game" class = "special-btn" onclick = "HardGame()">Disclose all thorns: <div class = "special-cost">50</div>
<div id = "not-rec">(NOT RECOMMENDED)</div></div>

            <div id = "follow">
            
    <div id = "follow-question">Are you following me?</div>
     
           <div id = "follow-yes" class = "follow-answer" onclick = "FollowYes()">YES</div>
       
         <div id = "follow-no" class = "follow-answer" onclick = "FollowNo()">NO</div>
   
         </div>
        
    <div id = "tutorials">TUTORIALS</div>
      
      <div id = "excuse">(The videos are laggy because my laptop couldn't handle the screen recorder)</div>
    
        <div class = "tut-lvl">
      
          <div class = "tl-heading">LEVEL 1</div>
    
            <video controls style="outline:none;">
        
            <source src="https://drive.google.com/uc?export=download&id=1V4iG-zV8xAWMzcC01CeD74-O3rhUZ1iY">
        
        </video>
    
        </div>
   
         <div class = "tut-lvl">
     
           <div class = "tl-heading">LEVEL 2</div>
       
         <video controls style="outline:none;">
        
            <source src="https://drive.google.com/uc?export=download&id=1RhMIKghknL8XVXYJv1XyfUl7jqSed-__">
      
          </video>
    
        </div>
   
         <div class = "tut-lvl">
  
              <div class = "tl-heading">LEVEL 3</div>
   
             <video controls style="outline:none;">
        
            <source src="https://drive.google.com/uc?export=download&id=13UAX8skp8KJrIVTbowC5-CkbGUj2XbGJ">
       
         </video>
   
         </div>
       
     <div class = "tut-lvl">
    
            <div class = "tl-heading">LEVEL 4</div>
        
        <video controls style="outline:none;">
       
             <source src="https://drive.google.com/uc?export=download&id=1OkrtZbCbK6PHz5FFMGcy4VaJcp_oXxhx">
         
       </video>
     
       </div>
   
         <div class = "tut-lvl">
        
        <div class = "tl-heading">LEVEL 5</div>
         
       <video controls style="outline:none;">
       
             <source src="https://drive.google.com/uc?export=download&id=1jRW4SHKK6G6QQRqdypE1xnYtF_TmZoQD">
          
      </video>
   
         </div>
     
       <br><br><br>
      
      <div id = "shop-back" onclick = "CloseShop()">BACK</div>
     
   </div>
   
     <div id = "game1" class = "game">
     
       <div class = "mario"></div>
    
        <div id = "a" class = "object land"></div>
      
      <div id = "b" class = "object land"></div>
   
         <div id = "c" class = "object land"></div>
       
     <div id = "d" class = "object box"></div>
     
       <div id = "e" class = "object box"></div>
  
          <div id = "f" class = "object land"></div>
     
       <div id = "g" class = "object land"></div>
   
         <div id = "h" class = "object box"></div>
   
         <div id = "i" class = "object spikes"></div>
     
       <div id = "j" class = "object spikes"></div>
       
     <div id = "k" class = "object spikes"></div>
      
      <div id = "l" class = "object flag end"></div>
    
        <div id = "m" class = "object stump end"></div>
      
      <div id = "n" class = "object end"></div>
    
        <div id = "o" class = "object coin"></div>
    
        <div id = "p" class = "object coin"></div>
    
        <div id = "q" class = "object coin"></div>
        
    <div id = "r" class = "object coin"></div>
    
    </div>
        <div id = "game2" class = "game">
      
      <div class = "mario"></div>
  
          <div id = "aa" class = "object land"></div>
      
      <div id = "ab" class = "object box"></div>
    
        <div id = "ac" class = "object box"></div>
      
      <div id = "ad" class = "object box"></div>
      
      <div id = "ae" class = "object box"></div>
  
          <div id = "af" class = "object box"></div>
        
    <div id = "ag" class = "object spikes"></div>
     
       <div id = "ah" class = "object spikes"></div>
    
        <div id = "ai" class = "object spikes"></div>
     
       <div id = "aj" class = "object box"></div>
      
      <div id = "ak" class = "object spikes"></div>
   
         <div id = "al" class = "object land"></div>
    
        <div id = "am" class = "object land"></div>
     
       <div id = "an" class = "object land"></div>
     
       <div id = "ao" class = "object weak-land"></div>
     
       <div id = "ap" class = "object weak-land"></div>
     
       <div id = "aq" class = "object spikes"></div>
    
        <div id = "ar" class = "object box"></div>
   
         <div id = "as" class = "object land"></div>
    
        <div id = "at" class = "object flag end"></div>
      
      <div id = "au" class = "object stump end"></div>
      
      <div id = "av" class = "object coin"></div>
    
        <div id = "aw" class = "object coin"></div>
   
         <div id = "ax" class = "object coin"></div>
    
        <div id = "ay" class = "object box"></div>
    
        <div id = "az" class = "object spikes"></div>
      
      <div id = "ba" class = "object box"></div>
    
        <div id = "bb" class = "object spikes"></div>
   
         <div id = "bc" class = "object coin"></div>
    
    </div>
        <div id = "game3" class = "game">
     
       <div class = "mario"></div>
     
       <div id = "ca" class = "object land"></div>
  
          <div id = "cb" class = "object box"></div>
    
        <div id = "cc" class = "object box"></div>
    
        <div id = "cd" class = "object creature"></div>
      
      <div id = "ce" class = "object spikes"></div>
    
        <div id = "cf" class = "object weak-land"></div>
     
       <div id = "cg" class = "object land"></div>
     
       <div id = "ch" class = "object spikes"></div>
    
        <div id = "ci" class = "object box"></div>
    
        <div id = "cj" class = "object land"></div>
    
        <div id = "ck" class = "object land"></div>
    
        <div id = "cl" class = "object coin"></div>
    
        <div id = "cm" class = "object land"></div>
   
         <div id = "cn" class = "object weak-land"></div>
   
         <div id = "co" class = "object land"></div>
    
        <div id = "cp" class = "object coin"></div>
     
       <div id = "cq" class = "object box"></div>
    
        <div id = "cr" class = "object spikes"></div>
     
       <div id = "cs" class = "object spikes"></div>
    
        <div id = "ct" class = "object spikes"></div>
    
        <div id = "cu" class = "object land"></div>
    
        <div id = "cv" class = "object land"></div>
      
      <div id = "cw" class = "object land"></div>
     
       <div id = "cx" class = "object creature"></div>
   
         <div id = "cy" class = "object spikes"></div>
    
        <div id = "cz" class = "object land"></div>
     
       <div id = "da" class = "object flag end"></div>
       
     <div id = "db" class = "object stump end"></div>
       
     <div id = "dc" class = "object spikes"></div>
       
     <div id = "dd" class = "object coin"></div>
    
        <div id = "de" class = "object coin"></div>
    
    </div>
      
  <div id = "game4" class = "game">
        
    <div class = "mario"></div>
  
          <div id = "ea" class = "object land"></div>
    
        <div id = "eb" class = "object weak-land"></div>
    
        <div id = "ec" class = "object land"></div>
    
        <div id = "ed" class = "object land"></div>
    
        <div id = "ee" class = "object spikes"></div>
     
       <div id = "ef" class = "object cannonball"></div>
     
       <div id = "eg" class = "object cannon"></div>
      
      <div id = "eh" class = "object land"></div>
     
       <div id = "ei" class = "object weak-land"></div>
    
        <div id = "ej" class = "object spikes"></div>
     
       <div id = "ek" class = "object box"></div>
     
       <div id = "el" class = "object spikes"></div>
     
       <div id = "em" class = "object box"></div>
     
       <div id = "en" class = "object coin"></div>
     
       <div id = "eo" class = "object land"></div>
     
       <div id = "ep" class = "object spikes"></div>
     
       <div id = "eq" class = "object land"></div>
    
        <div id = "er" class = "object land"></div>
     
       <div id = "es" class = "object land"></div>
       
     <div id = "et" class = "object cannonball"></div>
      
      <div id = "eu" class = "object cannon"></div>
     
       <div id = "ev" class = "object cannonball"></div>
     
       <div id = "ew" class = "object cannon"></div>
   
         <div id = "ex" class = "object land"></div>
     
       <div id = "ey" class = "object creature"></div>
       
     <div id = "ez" class = "object land"></div>
    
        <div id = "fa" class = "object flag end"></div>
    
        <div id = "fb" class = "object stump end"></div>
    
        <div id = "fc" class = "object land"></div>
     
       <div id = "fd" class = "object coin"></div>
    
        <div id = "fe" class = "object coin"></div>
     
       <div id = "ff" class = "object coin"></div>
   
     </div>
    
    <div id = "game5" class = "game">
    
        <div class = "mario"></div>
    
        <div id = "ga" class = "object land"></div>
       
     <div id = "gb" class = "object box"></div>
       
     <div id = "gc" class = "object box"></div>
      
      <div id = "gd" class = "object box"></div>
            <div id = "ge" class = "object coin"></div>
            <div id = "gf" class = "object box"></div>
            <div id = "gg" class = "object box"></div>
            <div id = "gh" class = "object creature"></div>
            <div id = "gi" class = "object spikes"></div>
            <div id = "gj" class = "object spikes"></div>
            <div id = "gk" class = "object box"></div>
            <div id = "gl" class = "object weak-land left-right"></div>
            <div id = "gm" class = "object moving-land"></div>
            <div id = "gn" class = "object land"></div>
            <div id = "go" class = "object land"></div>
            <div id = "gp" class = "object land"></div>
            <div id = "gq" class = "object land"></div>
            <div id = "gr" class = "object spikes"></div>
            <div id = "gs" class = "object moving-land up-down"></div>
            <div id = "gt" class = "object coin"></div>
            <div id = "gu" class = "object cannonball"></div>
            <div id = "gv" class = "object cannon"></div>
            <div id = "gw" class = "object land"></div>
            <div id = "gx" class = "object land"></div>
            <div id = "gy" class = "object land"></div>
            <div id = "gz" class = "object land"></div>
            <div id = "ha" class = "object flag end"></div>
            <div id = "hb" class = "object stump end"></div>
            <div id = "hc" class = "object coin"></div>
            <div id = "hd" class = "object moving-land left-right"></div>
            <div id = "he" class = "object cannonball"></div>
            <div id = "hf" class = "object cannon"></div>
            <div id = "hg" class = "object land"></div>
            <div id = "hh" class = "object land"></div>
        </div>
        <div id = "dark"></div>
        <div id = "lost" class = "result">
            <div class = "heading">YOU LOST</div>
            <button class = "btn" onclick = "Replay()">REPLAY</button>
            <button class = "btn menu-btn" onclick = "ShowMenu()">MENU</button>
        </div>
        <div id = "won" class = "result">
            <div class = "heading">YOU WON</div>
            <button class = "btn" onclick = "Replay()">REPLAY</button>
            <button class = "btn menu-btn" onclick = "ShowMenu()">MENU</button>
            <button class = "btn next-lvl" onclick = "NextLevel()">NEXT LEVEL</button>
        </div>
        <div id = "coins"><div id = "coins-count"></div></div>
        <div id = "alert-background">
            <div id = "alert">
                <div id = "alert-heading"></div>
                <div id = "alert-text"></div>
                <div id = "alert-illustration"></div>
                <div id = "alert-button" onclick = "Close();">CLOSE</div>
            </div>
        </div>
        <div id = "plus-ten">+10</div>
        <div id = "notif"></div>
        <div id = "btn-left" class = "controls">LEFT</div>
        <div id = "btn-right" class = "controls">RIGHT</div>
        <div id = "btn-up" class = "controls">JUMP</div>
        <div id = "show-hide-btn" onclick = "ShowHideButton()">HIDE BUTTONS</div>
        <div id = "restart-btn" onclick = "restartLevel()">RESTART</div>
        <div id = "progress-bar">
            <div id = "progress"></div>
        </div>
    </div></body>
</html>
