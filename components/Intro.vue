<template>
  <section class="intro">
    <div class="logo">
      <img src="../assets/images/uphellas-logo.svg" alt="" />
    </div>
    <div class="intro-container">
      <div class="intro-left-section">
        <img id="badge" src="../assets/images/5-badge.svg" />
        <div id="crazy-thought">
          <h1>HERE'S A</h1>
          <h1>CRAZY THOUGHT</h1>
        </div>
        <p>Happy & healthy employees work better!</p>
        <button @click="scrollToCards">FIND OUT HOW WE CAN HELP YOU</button>
      </div>
      <div class="intro-right-section">
        <img id="banner-img" src="../assets/images/banner-image.png" />
      </div>
    </div>
    <div class="scroll-button">
      <p>SCROLL FOR MORE</p>
      <!-- <img src="../assets/images/" /> -->
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="#fff"
        class="bi bi-chevron-down"
        viewBox="0 0 16 16"
      >
        <path
          fill-rule="evenodd"
          d="M1.646 4.646a.5.5 0 0 1 .708 0L8 10.293l5.646-5.647a.5.5 0 0 1 .708.708l-6 6a.5.5 0 0 1-.708 0l-6-6a.5.5 0 0 1 0-.708z"
        />
      </svg>
    </div>
  </section>
  <Intro_cards />
</template>

<script>
export default {
  name: "Intro",
  methods: {
    scrollToCards() {
      const cardsSection = document.querySelector(".intro-cards-text");

      cardsSection.scrollIntoView({behavior: "smooth"});
    },
  },
};
</script>

<style>
.intro {
  background-color: #fb8500;
  padding: 3rem 5rem 8rem 5rem;
  font-family: "cf_astylight", sans-serif;
  position: relative;
}

.logo {
  display: grid;
  place-items: center;
}

.logo img {
  width: 15vw;
}

.intro-container {
  display: flex;
  justify-content: space-between;
}

#badge {
  position: absolute;
  left: 26%;
}

#crazy-thought {
  margin-top: 7.2rem;
  color: #8ecae6;
  font-size: 1.4vw;
  line-height: 3vw;
  /* transform: rotate(-4deg); */
  transform: skew(0, -5deg);
  position: absolute;
  text-shadow: 3px 4px 3px rgba(0, 0, 0, 0.836),
    3px 1px 1px rgba(0, 0, 0, 0.233);
}

.intro-left-section p {
  margin-top: 6rem;
  margin-left: 2rem;
  color: #fff;
  font-size: clamp(1rem, 3vw, 4rem);
  margin-top: 16rem;
  max-width: 40%;
  font-weight: bold;
}

.intro-left-section button {
  margin-top: 3rem;
  font-weight: bold;
  font-size: 1.23vw;
  margin-left: 2rem;
  padding: 0.8vw;
  border-radius: 26px;
  border: 3px solid #000;
  box-shadow: -3px 3px 3px #000;
  cursor: pointer;
}

#banner-img {
  position: absolute;
  right: 2.5%;
  top: 25%;
  max-width: 45%;
}

.scroll-button {
  display: grid;
  place-items: center;
  margin-top: 10rem;
}

.scroll-button p {
  font-weight: bold;
  font-size: 1.3vw;
  margin-bottom: 0.5rem;
}

.scroll-button svg {
  transform: scale(1.6);
}

@media (max-width: 1650px) {
  .intro-left-section p {
    margin-top: 15rem !important;
  }

  #banner-img {
    right: 4.5% !important;
  }
}

@media (max-width: 1350px) {
  .intro-left-section p {
    margin-top: 14rem !important;
  }

  .intro-left-section button {
    margin-top: 2rem !important;
  }

  #banner-img {
    top: 29% !important;
  }

  #badge {
    transform: scale(0.8);
  }
}

@media (max-width: 1100px) {
  .intro {
    padding: 3rem 4rem 4rem 4rem !important;
  }

  .intro-left-section p {
    margin-top: 13rem !important;
  }

  #badge {
    transform: scale(0.75);
  }

  #banner-img {
    top: 31% !important;
  }
}

@media (max-width: 950px) {
  .scroll-button {
    margin-top: 5rem !important;
  }

  .scroll-button svg {
    transform: scale(1.3) !important;
  }

  .intro-left-section p {
    margin-top: 12.5rem !important;
    margin-left: 1.5rem !important;
  }

  .intro-left-section button {
    margin-top: 1.5rem !important;
    margin-left: 1.5rem !important;
  }

  #banner-img {
    top: 35% !important;
  }

  #badge {
    transform: scale(0.72);
  }
}

@media (max-width: 800px) {
  #banner-img {
    top: 40% !important;
  }

  #badge {
    transform: scale(0.67) !important;
  }

  .intro {
    padding: 2rem !important;
  }

  .intro-left-section p {
    margin-top: 11.5rem !important;
  }
}

@media (max-width: 750px) {
  .intro {
    padding: 0 2rem !important;
  }

  .scroll-button {
    margin-top: 3rem !important;
  }

  #banner-img {
    top: 40% !important;
  }

  #badge {
    transform: scale(0.6) !important;
  }

  .scroll-button svg {
    transform: scale(1.1);
  }

  .intro-left-section button {
    border: 2px solid #000;
  }
}

@media (max-width: 620px) {
  #banner-img {
    top: 42% !important;
  }

  .intro-left-section p {
    margin-top: 11rem !important;
  }

  .intro-left-section button {
    margin-top: 1rem !important;
  }

  #badge {
    transform: scale(0.57) !important;
  }
}

@media (max-width: 525px) {
  #banner-img {
    top: 45% !important;
  }

  #crazy-thought {
    margin-top: 7.7rem !important;
  }

  #badge {
    left: 20% !important;
    transform: scale(0.48) !important;
  }

  .intro-left-section p {
    margin-top: 11rem !important;
  }

  .intro-left-section button {
    margin-top: 1rem !important;
  }

  .scroll-button svg {
    height: 1rem !important;
    width: 0.8rem !important;
  }
}

@media (max-width: 495px) {
  .intro-left-section p {
    margin-top: 10.5rem !important;
  }

  .intro-left-section button {
    margin-top: 0.7rem !important;
  }

  #banner-img {
    top: 44% !important;
  }

  #badge {
    transform: scale(0.4) !important;
    left: 22% !important;
  }
}

@media (max-width: 430px) {
  #crazy-thought {
    margin-top: 8rem !important;
  }

  .intro {
    padding: 1rem !important;
  }
}

@media (max-width: 395px) {
  #banner-img {
    top: 46.5% !important;
  }
}
</style>
