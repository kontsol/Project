<template>
  <section class="card-review-gift">
    <div class="card-review-container">
      <div class="card-review-image-section">
        <img
          style="width: 98%"
          id="perfectgift-image"
          src="../assets/images/upgift.png"
          alt=""
        />
      </div>
      <div class="card-review-text-section">
        <div class="unrivalled-meal">
          <p>THE PERFECT GIFT</p>
        </div>
        <div class="card-review-content">
          <div
            class="card-review-logo"
            style="gap: 0rem; transform: translateX(-5.3%)"
          >
            <img id="up-gift" src="../assets/images/UP-GIFT.svg" />
            <h1
              style="background-color: #a6351d; transform: translateX(-20.3%)"
            >
              GIFT CARD
            </h1>
          </div>
          <h2>Enjoy your meals anywhere you want</h2>
          <p id="card-review-describe">
            Our reloadable gift card is the perfect gift to reward, to
            incentivise, to celebrate!
          </p>
          <p id="card-review-price" style="width: 24.2rem">
            Tax exemption: 300 euros per year per employee
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
          </div>
          <div
            @click="scrollToForm"
            class="card-review-button"
            style="background-color: #a6351d"
          >
            <button style="background-color: #a6351d">TELL ME MORE</button>
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
    </div>
  </section>
</template>
<script>
export default {
  name: "CardReview_GiftCard",
  methods: {
    scrollToForm() {
      const formSection = document.querySelector(".footer-container");

      formSection.scrollIntoView({behavior: "smooth"});
    },
  },
};
</script>
<style>
.card-review-gift {
  background-color: #a6351d;
  padding: 5rem 7rem;
  font-family: "cf_astylight", sans-serif;
}

.card-review-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
}

.card-review-image-section img {
  width: 85%;
}

.card-review-button svg {
  width: 1.5rem;
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
  text-shadow: 3px 4px 3px rgba(0, 0, 0, 0.5);
  transform: rotate(-4deg);
  margin-bottom: 2.2rem;
}

.card-review-logo {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.card-review-logo h1 {
  color: #fff;
  background-color: #f4a261;
  font-size: 0.8rem;
  padding: 0.3rem 0.6rem;
  border-radius: 26px;
}

.card-review-logo img {
  width: 11rem;
}

.card-review-content {
  padding: 1.5rem 2.5rem 6rem 2.5rem;
}

.card-review-content h2 {
  font-weight: bold;
  font-size: 2.2rem;
  width: 30rem;
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

@media (max-width: 1420px) {
  .card-review-gift {
    padding: 4rem 5rem !important;
  }
}

@media (max-width: 1050px) {
  .card-review-gift {
    padding: 3rem !important;
  }
}

@media (max-width: 770px) {
  .card-review-gift {
    padding: 2rem !important;
    overflow: hidden !important;
  }
}

@media (max-width: 550px) {
  .card-review-gift {
    padding: 1rem 1rem 5rem 1rem !important;
  }
}
</style>
