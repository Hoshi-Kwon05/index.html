<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Hart's Birthday 🎂</title>

<style>

/* =========================
   BASIC SETUP
========================= */

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    min-height: 100vh;
    font-family: Arial, sans-serif;
    background: #fff;
    color: #625b65;
    overflow-x: hidden;
}

/* SOFT BACKGROUND */

body::before {
    content: "";
    position: fixed;
    width: 280px;
    height: 280px;
    border-radius: 50%;
    background: #fff0f6;
    top: -140px;
    left: -140px;
    z-index: -1;
}

body::after {
    content: "";
    position: fixed;
    width: 280px;
    height: 280px;
    border-radius: 50%;
    background: #f0edff;
    right: -140px;
    bottom: -140px;
    z-index: -1;
}

/* =========================
   FLOATING DECOR
========================= */

.float {
    position: fixed;
    z-index: 20;
    cursor: pointer;
    color: #d69ab6;
    animation: float 4s ease-in-out infinite;
}

.f1 {
    top: 12%;
    left: 7%;
    font-size: 25px;
}

.f2 {
    top: 28%;
    right: 8%;
    font-size: 20px;
    animation-delay: 1s;
}

.f3 {
    bottom: 20%;
    left: 9%;
    font-size: 22px;
    animation-delay: 2s;
}

.f4 {
    bottom: 12%;
    right: 8%;
    font-size: 27px;
    animation-delay: 1.5s;
}

@keyframes float {

    0%, 100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-12px);
    }
}

/* =========================
   CONTAINER
========================= */

.container {
    width: min(92%, 560px);
    margin: auto;
    padding: 28px 0 60px;
}

/* =========================
   TOP PROGRESS
========================= */

.top {
    display: flex;
    justify-content: space-between;
    color: #aaa;
    font-size: 12px;
    margin-bottom: 10px;
}

.progress {
    height: 5px;
    background: #eee8ee;
    border-radius: 20px;
    overflow: hidden;
    margin-bottom: 25px;
}

.progress-fill {
    height: 100%;
    width: 14%;
    background: #d596b3;
    transition: .5s;
}

/* =========================
   PAGES
========================= */

.page {
    display: none;
}

.page.active {
    display: block;
    animation: appear .4s ease;
}

@keyframes appear {

    from {
        opacity: 0;
        transform: translateY(15px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* =========================
   CARD
========================= */

.card {
    background: rgba(255,255,255,.98);
    border: 1px solid #eee8ee;
    border-radius: 28px;
    padding: 38px 25px;
    text-align: center;
    box-shadow: 0 12px 35px rgba(80,60,80,.08);
}

.emoji {
    font-size: 55px;
    margin-bottom: 15px;
    animation: bounce 2s infinite;
}

@keyframes bounce {

    0%, 100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-8px);
    }
}

h1 {
    color: #d28da9;
    font-size: clamp(34px, 9vw, 48px);
    margin-bottom: 15px;
}

h2 {
    color: #8975b3;
    font-size: clamp(24px, 7vw, 34px);
    margin-bottom: 15px;
}

p {
    line-height: 1.7;
    margin-bottom: 18px;
}

/* =========================
   BUTTONS
========================= */

button {
    border: none;
    border-radius: 50px;
    padding: 14px 23px;
    min-height: 48px;
    font-size: 15px;
    font-weight: bold;
    cursor: pointer;
    transition: .25s;
}

button:hover {
    transform: translateY(-3px);
}

button:active {
    transform: scale(.95);
}

.primary {
    background: #d596b3;
    color: white;
}

.purple {
    background: #9583bf;
    color: white;
}

.light {
    background: #faf8fb;
    color: #786b80;
    border: 1px solid #e3dbe5;
}

/* =========================
   NO BUTTON
========================= */

#noButton {
    position: relative;
}

/* =========================
   QUIZ / RESULTS
========================= */

.quiz-options {
    display: grid;
    gap: 12px;
    margin: 20px 0;
}

.quiz-option {
    border: 1px solid #e4dce6;
    border-radius: 18px;
    padding: 16px;
    cursor: pointer;
    transition: .25s;
    background: white;
    color: #625b65;
}

.quiz-option:hover {
    background: #fff5f8;
    transform: translateY(-2px);
}

.quiz-result {
    min-height: 30px;
    color: #d28da9;
    font-weight: bold;
}

/* =========================
   DATE PICKER
========================= */

.date-box {
    margin: 25px 0;
}

#birthdayDate {
    width: 100%;
    padding: 16px;
    border-radius: 18px;
    border: 1px solid #e4dce6;
    background: #fffafd;
    color: #625b65;
    font-size: 16px;
    text-align: center;
    outline: none;
    cursor: pointer;
}

#birthdayDate:focus {
    border-color: #d596b3;
    box-shadow: 0 0 0 3px #fff0f6;
}
/* =========================
   GIFTS
========================= */

.gifts {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
    margin: 25px 0;
}

.gift {
    font-size: 55px;
    padding: 18px 8px;
    border-radius: 20px;
    background: #fffafd;
    border: 1px solid #eadfe8;
    cursor: pointer;
    transition: .3s;
}

.gift:hover {
    transform: translateY(-8px) rotate(2deg);
}

.gift.opened {
    transform: scale(1.05);
    background: #fff5f8;
}

/* =========================
   CAKE
========================= */

.cake {
    font-size: 105px;
    cursor: pointer;
    display: inline-block;
    transition: .3s;
    user-select: none;
}

.cake:hover {
    transform: scale(1.08);
}

.cake:active {
    transform: scale(.9);
}

.cake-message {
    color: #d28da9;
    font-weight: bold;
    min-height: 30px;
}

/* =========================
   LETTER
========================= */

.letter {
    text-align: left;
    background: #fffafd;
    border: 1px solid #efdde5;
    border-radius: 20px;
    padding: 22px;
    margin: 20px 0;
}

.signature {
    text-align: right;
    color: #c987a5;
    font-weight: bold;
   }
   /* =========================
   STAR CONFETTI
========================= */

.confetti {
    position: fixed;
    top: -30px;
    z-index: 100;
    pointer-events: none;
    animation: fall linear forwards;
}

@keyframes fall {

    to {
        transform:
            translateY(110vh)
            rotate(720deg);
    }
}

/* =========================
   BALLOON CONFETTI
========================= */

.balloon-confetti {
    position: fixed;
    bottom: -100px;
    z-index: 150;
    pointer-events: none;
    animation: balloonFly 3s ease-out forwards;
    user-select: none;
}

@keyframes balloonFly {

    0% {
        transform:
            translateY(0)
            translateX(0)
            rotate(0deg)
            scale(.7);
        opacity: 0;
    }

    10% {
        opacity: 1;
    }

    60% {
        transform:
            translateY(-65vh)
            translateX(var(--side))
            rotate(var(--rotate))
            scale(1.1);
        opacity: 1;
    }

    100% {
        transform:
            translateY(-120vh)
            translateX(calc(var(--side) * 1.5))
            rotate(var(--rotate));
        opacity: 0;
    }
}

/* =========================
   HEART BURST
========================= */

.heart {
    position: fixed;
    pointer-events: none;
    z-index: 100;
    color: #d596b3;
    font-size: 25px;
    transition: 1s ease;
}

/* =========================
   FINAL
========================= */

.final-box {
    margin-top: 20px;
    padding: 22px;
    border-radius: 20px;
    background: #fff7fa;
    color: #c987a5;
    font-weight: bold;
}

/* =========================
   MOBILE
========================= */

@media(max-width:450px) {

    .card {
        padding: 32px 19px;
    }

    .gifts {
        gap: 8px;
    }

    .gift {
        font-size: 43px;
    }

    button {
        width: 100%;
    }

}

</style>
</head>

<body>

<!-- FLOATING CLICKABLE DECOR -->

<div class="float f1" onclick="heartBurst()">♡</div>
<div class="float f2" onclick="heartBurst()">✦</div>
<div class="float f3" onclick="heartBurst()">✧</div>
<div class="float f4" onclick="heartBurst()">♡</div>

<div class="container">

<!-- TOP PROGRESS -->

<div class="top">

    <span id="label">
        BIRTHDAY CHECK
    </span>

    <span id="number">
        1 / 7
    </span>

</div>

<div class="progress">

    <div
        class="progress-fill"
        id="progress"
    ></div>

</div>

<!-- =========================
     PAGE 1
========================= -->

<section
    class="page active"
    id="page1"
>

<div class="card">

    <div class="emoji">
        🚨
    </div>

    <h1>
        AYSA.
    </h1>

    <p>
        Mandatory checkpoint ni.
    </p>

    <h2>
        Are you Hart?
    </h2>

    <div style="
        display:flex;
        gap:10px;
        justify-content:center;
        margin-top:20px;
    ">

        <button
            class="primary"
            onclick="nextPage(2)"
        >
            malamang??
        </button>

        <button
            class="light"
            id="noButton"
        >
            dili daw
        </button>

    </div>

</div>

</section>

<!-- =========================
     PAGE 2
========================= -->

<section
    class="page"
    id="page2"
>

<div class="card">

    <div class="emoji">
        📅
    </div>

    <h2>
        AYSA for the 2nd time...
    </h2>

    <p>
        Anoe bd date?
    </p>

    <p>
        Use the calendar
    </p>

    <div class="date-box">

        <input
            type="date"
            id="birthdayDate"
            min="2020-01-01"
            max="2035-12-31"
        >

    </div>

    <button
        class="primary"
        onclick="checkDate()"
    >
        Chakto?? →
    </button>

    <div
        class="quiz-result"
        id="quizResult"
        style="margin-top:20px;"
    ></div>

</div>

</section>

<!-- =========================
     PAGE 3
========================= -->

<section
    class="page"
    id="page3"
>

<div class="card">

    <div class="emoji">
        🎁
    </div>

    <h2>
        Pasado lods
    </h2>

    <p>
        Pera o kahon?
        <br>
        Ps. way kwarta
    </p>

    <div class="gifts">

        <div
            class="gift"
            onclick="openGift(this,1)"
        >
            🎁
        </div>

        <div
            class="gift"
            onclick="openGift(this,2)"
        >
            🎁
        </div>

        <div
            class="gift"
            onclick="openGift(this,3)"
        >
            🎁
        </div>

    </div>

    <div
        id="giftResult"
        class="quiz-result"
    >
        pili lng...
    </div>

</div>

</section>

<!-- =========================
     PAGE 4
========================= -->

<section
    class="page"
    id="page4"
>

<div class="card">

    <div class="emoji">
        🎂
    </div>

    <h2>
        Virtual cake!!
    </h2>

    <p>
        Happy Birthday babyshark
    </p>

    <p>
        <strong>
   Tap the cake
        </strong>
    </p>

    <div
        class="cake"
        id="cake"
        onclick="cakeClick()"
    >
        🎂
    </div>

    <p id="candles">
        🕯️ 🕯️ 🕯️ 🕯️ 🕯️
    </p>

    <div
        class="cake-message"
        id="cakeMessage"
    >
        The candles are waiting...
    </div>

</div>

</section>

<!-- =========================
     PAGE 5
========================= -->

<section
    class="page"
    id="page5"
>

<div class="card">

    <div class="emoji">
        💌
    </div>

    <h2>
        HAPPY BIRTHDAY HART!!
    </h2>

    <div class="letter">

        <p>
            My dearest, Hart
        </p>

        <p>
            Happy birthday bb
        </p>

        <p>
            Congrats on surviving another year.
            Despite all the challenges, thank you for staying, hart.
        </p>

        <p>
            This is just a little appreciation and a reminder
            of how much u are loved, hart. Thank you sm for being
            such a great friend, for staying, listening, understanding,
            and simply being there. Ik a lot has happened, and ik how
            much u’ve had to survive, sacrifice, and endure. You’ve been
            through things that weren’t always easy, and yet u still
            chose to keep going and stay strong. I’ll always be proud
            of u for that.
        </p>

        <p>
            Please always remember that u don’t have to carry everything
            by urself. I’m here for you, hart, as ur shoulder to lean on,
            ur person to laugh with, someone to listen to ur rants,
            and someone who will stay even on the days when u don’t feel
            like talking. U can always come to me, whether u need someone
            to listen, someone to distract u, or someone to simply sit
            with u through whatever ur feeling.
        </p>

        <p>
            I hope u know how much u mean to the people around u.
            U deserve to be appreciated, cared for, and reminded that
            u are doing enough. Even when u doubt urself, I hope u
            remember that there are people who see ur effort, ur kindness,
            and how hard u try.
        </p>

        <p>
            Thank you for being u, hart. Thank you for letting me be part
            of ur life and for giving me so many reasons to be grateful
            for our friendship. I may not always know the right words
            to say or the perfect way to help, but I’ll always try.
            I’m always rooting for u, always proud of u, and always here
            whenever u need me.
        </p>

        <p>
            Stay funny, stay chaotic, and please
            continue being you.
        </p>

        <p class="signature">
            —Luvni mwamwa
        </p>

    </div>

    <button
        class="purple"
        onclick="nextPage(6)"
    >
        One more thing →
    </button>

</div>

</section>

<!-- =========================
     PAGE 6
========================= -->

<section
    class="page"
    id="page6"
>

<div class="card">

    <div class="emoji">
        🎈
    </div>

    <h2>
        BIRTHDAY CHALLENGE
    </h2>

    <p>
        Lovelove balloons, so...
    </p>

    <div class="quiz-options">

        <button
            class="quiz-option"
            onclick="balloonAnswer(1)"
        >
            1. Just one.
        </button>

        <button
            class="quiz-option"
            onclick="balloonAnswer(99)"
        >
            99. Obviously.
        </button>

        <button
            class="quiz-option"
            onclick="balloonAnswer(999)"
        >
            999. CHAOS.
        </button>

    </div>

    <div
        id="balloonResult"
        class="quiz-result"
    ></div>

</div>

</section>
<!-- =========================
     PAGE 7
========================= -->

<section
    class="page"
    id="page7"
>

<div class="card">

    <div class="emoji">
        🏆
    </div>

    <h1>
        HAPPY BIRTHDAY!
    </h1>

    <h2>
        Hart bb
    </h2>

    <p>
        You successfully completed
        the extremely unnecessary
        birthday investigation
    </p>

    <p>
        Your reward:
        <br>
        <strong>
            another year of being iconic
        </strong>
    </p>

    <button
        class="primary"
        onclick="finalChaos()"
    >
        PRESS FOR CHAOS 🎉
    </button>

    <div id="final"></div>

</div>

</section>

</div>

<script>

/* =========================
   PAGE SYSTEM
========================= */

let currentPage = 1;

const labels = [
    "BIRTHDAY CHECK",
    "DATE CHECK",
    "MYSTERY GIFTS",
    "CAKE EMERGENCY",
    "A LITTLE MESSAGE",
    "BIRTHDAY CHALLENGE",
    "FINAL LEVEL"
];

function nextPage(page) {

    document.querySelectorAll(".page")
    .forEach(function(item) {

        item.classList.remove("active");

    });

    const selectedPage =
        document.getElementById("page" + page);

    if (!selectedPage) return;

    selectedPage.classList.add("active");

    currentPage = page;

    document.getElementById(
        "number"
    ).textContent =
        page + " / 7";

    document.getElementById(
        "label"
    ).textContent =
        labels[page - 1];

    document.getElementById(
        "progress"
    ).style.width =
        ((page / 7) * 100) + "%";

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });
}


/* =========================
   RUNAWAY NO BUTTON
========================= */

const noButton =
    document.getElementById("noButton");

function runAway() {

    const x =
        Math.random() * 160 - 80;

    const y =
        Math.random() * 100 - 50;

    noButton.style.transform =
        "translate(" +
        x +
        "px," +
        y +
        "px)";

    const words = [
        "dili",
        "edi hawa diri",
        "di ligi",
        "di man kaha ikaw",
        "pahawa ngani",
        "buang, ingon dili"
    ];

    noButton.textContent =
        words[
            Math.floor(
                Math.random() * words.length
            )
        ];
}

noButton.addEventListener(
    "mouseenter",
    runAway
);

noButton.addEventListener(
    "touchstart",
    function(event) {

        event.preventDefault();

        runAway();

    }
);


/* =========================
   CALENDAR DATE CHECK
========================= */

function checkDate() {

    const dateInput =
        document.getElementById(
            "birthdayDate"
        );

    const result =
        document.getElementById(
            "quizResult"
        );

    if (!dateInput.value) {

        result.textContent =
            "pili sah date oy 😭";

        return;
    }

    const selectedDate =
        new Date(
            dateInput.value +
            "T00:00:00"
        );

    const month =
        selectedDate.getMonth() + 1;

    const day =
        selectedDate.getDate();

    if (
        month === 9 &&
        day === 28
    ) {

        result.innerHTML =
            "KOREK⭐";

        createConfetti();

        setTimeout(function() {

            nextPage(3);

        }, 1000);

    } else {

        result.textContent =
            "EKIS, imo bd wa ka kabalo, magon noon tika.";

    }
}


/* =========================
   GIFTS
========================= */

let giftOpened = false;

function openGift(element, number) {

    if (giftOpened) return;

    element.classList.add("opened");

    if (number === 1) {

        giftOpened = true;

        element.textContent = "🍰";

        document.getElementById(
            "giftResult"
        ).innerHTML = `

            YOU GOT CAKE 🍰

            <br><br>

            YAYAYYAYAYAYAYAYAY

            <br><br>

            <button
                class="purple"
                onclick="nextPage(4)"
            >
                Claim cake →
            </button>

        `;

        createConfetti();

    } else {

        element.textContent = "❌";

        document.getElementById(
            "giftResult"
        ).textContent =
            "Ekis, pili lain.";

        setTimeout(function() {

            element.textContent = "🎁";

            element.classList.remove(
                "opened"
            );

        }, 900);
    }
}


/* =========================
   CAKE
========================= */

let cakeDone = false;

function cakeClick() {

    if (cakeDone) return;

    cakeDone = true;

    document.getElementById(
        "candles"
    ).textContent =
        "💨 💨 💨 💨 💨";

    document.getElementById(
        "cake"
    ).style.transform =
        "scale(1.15)";

    document.getElementById(
        "cakeMessage"
    ).innerHTML = `

        <br>

        Ito lng afford ssob

        <br><br>

        <button
            class="purple"
onclick="nextPage(5)"
        >
            Continue →
        </button>

    `;

    createConfetti();
}


/* =========================
   BALLOON CHALLENGE
========================= */

function balloonAnswer(number) {

    const r
