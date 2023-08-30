<template>
  <section class="card-review-meal">
    <div class="card-review-container">
      <div class="card-review-text-section">
        <div class="unrivalled-meal">
          <p>THE UNRIVALLED MEAL</p>
          <p>CARD SOLUTION</p>
        </div>
        <div class="card-review-content">
          <div class="card-review-logo">
            <img src="../assets/images/go-for-eat.svg" />
            <h1>MEAL CARD</h1>
          </div>
          <h2>Enjoy your meals anywhere you want</h2>
          <p id="card-review-describe">
            Our prepaid meal card by Mastercard is designed to offer to both our
            corporate customers and users an unmatched experience that's simple
            & fun.
          </p>
          <p id="card-review-price">
            Tax exemption: 6 euros per day / 1,452 euros per year per employee
          </p>
          <p id="benefit">BENEFITS</p>
          <div class="card-review-benefits">
            <div class="benefit">
              <svg
                fill="#8ecae6"
                height="800px"
                width="800px"
                version="1.1"
                id="Capa_1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                viewBox="0 0 490.05 490.05"
                xml:space="preserve"
              >
                <g>
                  <g>
                    <path
                      d="M418.275,418.275c95.7-95.7,95.7-250.8,0-346.5s-250.8-95.7-346.5,0s-95.7,250.8,0,346.5S322.675,513.975,418.275,418.275
			z M157.175,207.575l55.1,55.1l120.7-120.6l42.7,42.7l-120.6,120.6l-42.8,42.7l-42.7-42.7l-55.1-55.1L157.175,207.575z"
                    />
                  </g>
                </g>
              </svg>
              <p>
                Order & load cards online in seconds, download invoices &
                reports in a click
              </p>
            </div>
            <div class="benefit">
              <svg
                fill="#8ecae6"
                height="800px"
                width="800px"
                version="1.1"
                id="Capa_1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                viewBox="0 0 490.05 490.05"
                xml:space="preserve"
              >
                <g>
                  <g>
                    <path
                      d="M418.275,418.275c95.7-95.7,95.7-250.8,0-346.5s-250.8-95.7-346.5,0s-95.7,250.8,0,346.5S322.675,513.975,418.275,418.275
			z M157.175,207.575l55.1,55.1l120.7-120.6l42.7,42.7l-120.6,120.6l-42.8,42.7l-42.7-42.7l-55.1-55.1L157.175,207.575z"
                    />
                  </g>
                </g>
              </svg>
              <p>
                Best in class service: Quantified & qualified with a monthly
                report
              </p>
            </div>
            <div class="benefit">
              <svg
                fill="#8ecae6"
                height="800px"
                width="800px"
                version="1.1"
                id="Capa_1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                viewBox="0 0 490.05 490.05"
                xml:space="preserve"
              >
                <g>
                  <g>
                    <path
                      d="M418.275,418.275c95.7-95.7,95.7-250.8,0-346.5s-250.8-95.7-346.5,0s-95.7,250.8,0,346.5S322.675,513.975,418.275,418.275
			z M157.175,207.575l55.1,55.1l120.7-120.6l42.7,42.7l-120.6,120.6l-42.8,42.7l-42.7-42.7l-55.1-55.1L157.175,207.575z"
                    />
                  </g>
                </g>
              </svg>
              <p>Our cards are accepted everywhere in Greece</p>
            </div>
            <div class="benefit">
              <svg
                fill="#8ecae6"
                height="800px"
                width="800px"
                version="1.1"
                id="Capa_1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                viewBox="0 0 490.05 490.05"
                xml:space="preserve"
              >
                <g>
                  <g>
                    <path
                      d="M418.275,418.275c95.7-95.7,95.7-250.8,0-346.5s-250.8-95.7-346.5,0s-95.7,250.8,0,346.5S322.675,513.975,418.275,418.275
			z M157.175,207.575l55.1,55.1l120.7-120.6l42.7,42.7l-120.6,120.6l-42.8,42.7l-42.7-42.7l-55.1-55.1L157.175,207.575z"
                    />
                  </g>
                </g>
              </svg>
              <p>Use our app for full control & mobile payments</p>
            </div>
          </div>
          <div @click="scrollToForm" class="card-review-button">
            <button>CONTACT US</button>
            <svg
              id="arrow-right"
              width="800px"
              height="800px"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M6 12H18M18 12L13 7M18 12L13 17"
                stroke="#000000"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </div>
          <div class="goforeat-card"></div>
        </div>
      </div>
      <div class="card-review-image-section">
        <img id="goforeat-image" src="../assets/images/goforeat.png" alt="" />
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "CardReview_MealCard",
  methods: {
    scrollToForm() {
      const formSection = document.querySelector(".footer-container");

      formSection.scrollIntoView({behavior: "smooth"});
    },
  },
};
</script>
<style>
.card-review-image-section {
  display: grid;
  place-items: center;
}

.card-review-meal {
  background-color: #ffbe0b;
  padding: 5rem 7rem;
  font-family: "cf_astylight", sans-serif;
  overflow: hidden !important;
}

.card-review-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  max-width: 100%;
}

.card-review-image-section img {
  max-width: 100%;
  overflow: auto;
}

.card-review-button svg {
  max-width: 1.5rem;
}

.card-review-content {
  background-color: #fff;
  position: relative;
  border-radius: 16px;
  border: 4px solid #000;
  box-shadow: -4px 4px 0px #000;
}

.unrivalled-meal {
  color: #8ecae6;
  font-weight: bold;
  text-shadow: 3px 4px 3px rgba(0, 0, 0, 0.836),
    3px 1px 1px rgba(0, 0, 0, 0.233);
  transform: skew(0, -5deg);

  margin-bottom: 2.2rem;
}

.unrivalled-meal p {
  font-size: 2.5vw;
}

.card-review-logo {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.card-review-logo h1 {
  text-align: center;
  color: #fff;
  background-color: #f4a261;
  font-size: 0.8rem;
  padding: 0.3rem 0.6rem;
  border-radius: 26px;
}

.card-review-logo img {
  width: 80rem;
}

.card-review-content {
  padding: 1.5rem 2.5rem 6rem 2.5rem;
}

.card-review-content h2 {
  font-weight: bold;
  font-size: 2.2vw;
  max-width: 75%;
  margin-top: 1.5rem;
}

#card-review-describe {
  margin-top: 2rem;
  line-height: 1.4rem;
  font-size: 1.2rem;
}

#card-review-price {
  margin-top: 1rem;
  background-color: #ececec;
  font-weight: bold;
  width: 33.3rem;
  padding: 0.5rem;
}

#benefit {
  font-weight: bold;
  margin-top: 1.7rem;
}

.card-review-benefits {
  margin-top: 0.7rem;
}

.benefit {
  display: flex;
  gap: 0.5rem;
  margin-bottom: 0.6rem;
}

.benefit svg {
  width: 1.2rem;
  height: 1.2rem;
}

#arrow-right {
  width: 2rem;
  height: 2rem;
}

.card-review-button {
  position: absolute;
  bottom: 0;
  right: -0.5%;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  background-color: #f4a261;
  padding: 0.6rem 2rem;
  border: 4px solid #000;
  box-shadow: -4px 4px 0px #000;
  border-radius: 16px 0px 16px 0;
}

.card-review-button button {
  border: none;
  background-color: #f4a261;
  color: #fff;
  font-weight: bold;
  font-size: 1.1rem;
}

@media (max-width: 1640px) {
  .card-review-container {
    gap: 4rem !important;
  }

  .card-review-image-section {
    display: grid;
    place-items: center;
  }

  .card-review-image-section img {
    transform: scale(1.2) !important;
  }
}

@media (max-width: 1420px) {
  .card-review-meal {
    padding: 4rem 5rem;
  }

  .card-review-logo h1 {
    padding: 0.1rem 0.4rem !important;
  }

  .card-review-content {
    padding-bottom: 4rem !important;
  }

  .card-review-content h2 {
    margin-top: 0.5rem !important;
  }

  #card-review-describe {
    margin-top: 1rem !important;
  }

  #benefit {
    margin-top: 1.2rem !important;
  }

  .card-review-benefits {
    margin-top: 0.4rem !important;
  }

  .card-review-button {
    padding: 0.4rem 1.8rem !important;
  }

  .card-review-image-section img {
    transform: scale(1.3) !important;
  }
}

@media (max-width: 1320px) {
  .card-review-image-section img {
    transform: scale(1.2) !important;
  }

  .card-review-content {
    padding: 1.2rem 2rem 3.5rem 2rem !important;
  }

  .card-review-content h2 {
    font-size: 1.8rem !important;
  }

  .card-review-content p {
    font-size: 0.9rem !important;
  }

  #card-review-price {
    width: 30rem !important;
  }
}

@media (max-width: 1200px) {
  .card-review-content {
    padding: 0.8rem 1.2rem 1.5rem 1.2rem !important;
  }

  .card-review-button {
    padding: 0.3rem 1rem !important;
    border: 3px solid #000 !important;
  }

  .card-review-button button {
    font-size: 0.9rem !important;
  }
}

@media (max-width: 1050px) {
  .card-review-meal {
    padding: 3rem !important;
  }

  .card-review-content {
    width: 28rem !important;
    height: 32rem !important;
  }

  #card-review-price {
    width: 22rem !important;
  }

  .card-review-image-section img {
    transform: scale(1.4) !important;
  }

  .card-review-content h2 {
    font-size: 1.4rem !important;
  }
}

@media (max-width: 900px) {
  .card-review-logo {
    gap: 0rem !important;
  }

  .card-review-logo img {
    transform: scale(0.9);
  }

  .card-review-content {
    width: 27rem !important;
    height: 32rem !important;
  }

  .card-review-image-section img {
    transform: scale(1.6) !important;
  }

  #card-review-price {
    width: 20rem !important;
  }

  .card-review-content h2 {
    margin-top: 0.5rem !important;
  }

  .card-review-button {
    padding-left: 0.3rem !important;
    padding-right: 0.3rem !important;
    gap: 0.2rem !important;
  }
}

@media (max-width: 850px) {
  .card-review-content {
    width: 25rem !important;
    height: 32rem !important;
  }

  .card-review-image-section img {
    transform: scale(1.6) !important;
  }

  .card-review-content h2 {
    font-size: 1.1rem !important;
  }

  .card-review-content p {
    font-size: 0.8rem !important;
    line-height: 1.1rem !important;
  }

  #card-review-price {
    font-size: 0.75rem !important;
    width: 17rem !important;
  }

  .card-review-button {
    padding: 0.05rem 0.5rem !important;
  }
  .card-review-button button {
    font-size: 0.6rem !important;
  }
}

@media (max-width: 770px) {
  .card-review-meal {
    padding: 2rem !important;
    overflow: hidden !important;
  }

  .card-review-content {
    width: 22rem !important;
    height: 32rem !important;
  }
  .card-review-image-section img {
    transform: scale(1.65) !important;
  }
}

@media (max-width: 680px) {
  .card-review-content {
    width: 20rem !important;
    height: 32.5rem !important;
  }

  #card-review-describe {
    line-height: 0.9rem !important;
  }

  .card-review-image-section img {
    transform: scale(1.8) !important;
  }

  .unrivalled-meal {
    margin-bottom: 1.5rem !important;
  }
}

@media (max-width: 610px) {
  .card-review-content {
    width: 18rem !important;
    height: 33rem !important;
  }

  #card-review-price {
    width: 15rem !important;
  }

  .card-review-logo h1 {
    font-size: 0.7rem !important;
    padding: 0.25rem 0rem !important;
  }

  .card-review-logo img {
    width: 8rem !important;
  }

  .card-review-logo {
    gap: 0 !important;
  }

  .card-review-logo h1 {
    width: 15rem !important;
  }

  .card-review-image-section img {
    transform: scale(2) !important;
  }

  .card-review-button {
    right: -1.5% !important;
  }
}

@media (max-width: 550px) {
  .card-review-meal {
    padding: 1rem 1rem 5rem 1rem !important;
  }

  .card-review-content {
    width: 16rem !important;
    height: 27rem !important;
  }

  #card-review-price {
    width: 11rem !important;
    font-size: 0.7rem !important;
    line-height: 0.7rem !important;
  }

  .card-review-logo h1 {
    font-size: 0.5rem !important;
    padding: 0.25rem 0rem !important;
    width: 4rem !important;
  }

  .card-review-logo img {
    width: 6rem !important;
  }

  .card-review-content h2 {
    font-size: 0.8rem !important;
    margin-top: 0.2rem !important;
  }

  .card-review-content p {
    margin-top: 0.5rem !important;
    font-size: 0.7rem !important;
    line-height: 0.8rem !important;
  }

  #benefit {
    margin-top: 0.5rem !important;
  }

  .benefit {
    margin-bottom: 0.2rem !important;
    align-items: center;
  }

  .card-review-button {
    right: -1.2% !important;
    padding: 0rem 0.3rem !important;
  }
}

@media (max-width: 470px) {
  .card-review-content {
    width: 14rem !important;
    height: 28rem !important;
  }

  .benefit {
    gap: 0.4rem !important;
    margin-bottom: 0rem !important;
  }
}

@media (max-width: 420px) {
  .card-review-image-section img {
    transform: scale(2.8) !important;
  }
}

@media (max-width: 380px) {
  .card-review-image-section img {
    transform: scale(4.5) !important;
  }
}
</style>
