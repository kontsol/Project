<template>
  <section class="intro-cards">
    <div class="intro-cards-text">
      <h1>Happy & healthy employees work better</h1>
      <p>
        We are Up. We design and deliver digital-first employee benefits that
        transform the workplace experience
      </p>
    </div>
    <div class="cards">
      <div class="card" @mouseenter="showButton" @mouseleave="hideButton">
        <img id="card-logo" src="../assets/images/go-for-eat.svg" />
        <p>The unrivalled meal card solution</p>
        <img id="card-banner" src="../assets/images/1.png" />
        <button v-show="isButtonVisible" class="learn-more-button">
          LEARN MORE
        </button>
      </div>
      <div class="card" @mouseenter="showButton" @mouseleave="hideButton">
        <img id="card-logo" src="../assets/images/UP-GIFT.svg" />
        <p>The perfect gift</p>
        <img id="card-banner" src="../assets/images/2.png" />
        <button v-show="isButtonVisible" class="learn-more-button">
          LEARN MORE
        </button>
      </div>
      <div class="card" @mouseenter="showButton" @mouseleave="hideButton">
        <img id="card-logo" src="../assets/images/up-cheque.svg" />
        <p>Where it all started our meal vouchers</p>
        <img id="card-banner" src="../assets/images/3.png" />
        <button v-show="isButtonVisible" class="learn-more-button">
          LEARN MORE
        </button>
      </div>
      <div class="card" @mouseenter="showButton" @mouseleave="hideButton">
        <img id="card-logo" src="../assets/images/up-holidays.svg" />
        <p>The card that takes you places</p>
        <img id="card-banner" src="../assets/images/4.png" />
        <button v-show="isButtonVisible" class="learn-more-button">
          LEARN MORE
        </button>
      </div>
      <div class="card" @mouseenter="showButton" @mouseleave="hideButton">
        <img id="card-logo" src="../assets/images/up-fit.svg" />
        <p>The multi-gym membership</p>
        <img id="card-banner" src="../assets/images/5.png" />
        <button v-show="isButtonVisible" class="learn-more-button">
          LEARN MORE
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Intro_cards",

  data() {
    return {
      isButtonVisible: false,
    };
  },
  methods: {
    showButton() {
      this.isButtonVisible = true;
    },
    hideButton() {
      this.isButtonVisible = false;
    },
  },
};
</script>

<style>
.intro-cards {
  background-color: #fb8500;
  font-family: "cf_astylight", sans-serif;
  padding: 4rem 0rem;
}

.intro-cards-text {
  display: grid;
  place-items: center;
  color: #fff;
}

.intro-cards-text h1 {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.intro-cards-text p {
  font-size: 1.1rem;
}

#heart-svg {
  width: 1rem;
}

.cards {
  margin-top: 6rem;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  cursor: pointer;
}

.card {
  min-height: 25rem;
  background-color: #ffbe0b;
  display: grid;
  place-items: center;
  border-radius: 16px;
  border: 2px solid #000;
  box-shadow: -3px 3px 3px #000;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  padding-top: 1rem;
  text-align: center;
  position: relative;
  transition: all 0.2s ease-in;
  font-size: 1.1rem;
}

.card:hover {
  background-color: #fff;
}

#card-logo {
  width: 11rem;
}

#card-banner {
  max-width: 80%;
}

.learn-more-button {
  display: none;
  position: absolute;
  bottom: 0;
  padding: 0.7rem 2.2rem;
  border: 3px solid #000;
  border-radius: 16px 16px 0 0;
  font-weight: bold;
  background-color: #ffbe0b;
}

.card:hover .learn-more-button {
  display: block;
}

@media (max-width: 850px) {
  .intro-cards {
    padding: 4rem 0 !important;
  }

  .intro-cards-text {
    padding: 0 3rem;
    text-align: center;
  }

  .cards {
    margin-top: 5rem !important;
  }
}

@media (max-width: 550px) {
  .intro-cards-text h1 {
    width: 75vw !important;
  }

  .intro-cards-text p {
    font-size: 1rem !important;
  }
}
</style>
