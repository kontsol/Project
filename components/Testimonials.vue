<template>
  <section class="testimonials">
    <div class="testimonials-container">
      <h2>Testimonials</h2>
      <div class="testimonials-text">
        <p>Need even more convincing?</p>
        <p>Here is what our customers say about us</p>
      </div>
      <div class="testimonials-reviews">
        <div class="testimonials-wrapper">
          <div
            v-for="testimonial in testimonials"
            :key="testimonial.id"
            class="testimonials-review"
          >
            <h1>{{ testimonial.title }}</h1>
            <p>{{ testimonial.body }}</p>
          </div>
        </div>
        <div class="testimonials-profile">
          <div v-for="(avatar, index) in avatars" :key="index">
            <img :src="avatar" alt="Avatar" />
          </div>
        </div>
      </div>
      <button id="load-more-button" @click="refreshReviews">Load more</button>

      <div class="testimonials-brands">
        <img id="brands" src="../assets/images/logo-1.svg" />
        <img id="brands" src="../assets/images/logo-2.svg" />
        <img id="brands" src="../assets/images/logo-3.svg" />
        <img id="brands" src="../assets/images/logo-4.svg" />
        <img id="brands" src="../assets/images/logo-5.svg" />
        <img id="brands" src="../assets/images/logo-6.svg" />
        <img id="brands" src="../assets/images/logo-7.svg" />
        <img id="brands" src="../assets/images/logo-8.svg" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "CardReview_MealCard",
  data() {
    return {
      testimonials: [],
      avatars: [],
    };
  },

  async mounted() {
    await this.fetchTestimonials();
    await this.randomAvatar();
  },
  methods: {
    async fetchTestimonials() {
      try {
        const response = await fetch(
          "https://jsonplaceholder.typicode.com/posts"
        );
        if (!response.ok) {
          throw new Error("Network response was not ok");
        }
        const data = await response.json();
        const randomData = this.randomDataArray(data);
        this.testimonials = randomData.slice(0, 2);
      } catch (error) {
        console.error("Error fetching testimonials:", error);
      }
    },

    randomDataArray(array) {
      for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [array[i], array[j]] = [array[j], array[i]];
      }
      return array;
    },

    refreshReviews() {
      this.fetchTestimonials();
    },
    // "xsgames.co/randomusers/avatar.php?g=male"
    async randomAvatar() {},
  },
};
</script>

<style>
.testimonials {
  background-color: #ffbe0b;
  font-family: "cf_astylight", sans-serif;
  padding: 6rem 2rem 3rem 2rem;
}

.testimonials-container {
  display: grid;
  place-items: center;
  gap: 1rem;
}

.testimonials-container h2 {
  font-size: 2.45vw;
  font-weight: bold;
}

.testimonials-text {
  text-align: center;
  font-size: 1.45vw;
  line-height: 1.5vw;
  margin-bottom: 1.5rem;
}

.testimonials-reviews {
  /* display: flex;
  align-items: center;
  white-space: nowrap; */
  /* gap: 1rem; */
  /* display: grid;
  grid-template-columns: repeat(2, 1fr); */
  /* display: flex;
  align-items: flex-start; */
  /* max-width: 80rem; */
  /* max-height: 19rem; */

  /* overflow-x: auto; */
}

.testimonials-wrapper {
  display: flex;
  flex-direction: row;
  gap: 2rem;
  /* margin-inline: 2rem; */
  /* width: 74rem; */
  /* white-space: nowrap; */
  /* overflow-y: auto; */
}

.testimonials-review {
  width: 38vw;
  height: 22rem;
  padding: 2rem 2rem 1rem 2rem;
  background-color: #fff;
  border-radius: 18px;
  display: flex;
  flex-direction: column;
}

.testimonials-review p {
  font-size: 1.6vw;
  color: #585858;
  line-height: 1.7vw;
  margin-top: 1vw;
}

.testimonials-review h1 {
  font-size: 1.8vw;
}

.testimonials-review-profile {
  display: flex;
  gap: 0.6rem;
}

.testimonials-review-profile img {
  max-width: 3rem;
  max-height: 3rem;
}

.testimonials-brands {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

#brands {
  margin-top: 1.8vw;
  filter: grayscale(100%) opacity(0.7);
  transform: scale(0.9);
}

#brands:hover {
  filter: opacity(1); /* Fully opaque on hover */
}

#load-more-button {
  border-radius: 24px;
  border: 3px solid #000;
  box-shadow: -3px 3px 0px #000;
  outline: none;
  font-size: 1.8vw;
  padding: 0.4rem 1rem;
  cursor: pointer;
  font-weight: bold;
  margin-top: 0.5rem;
}

@media (max-width: 1600px) {
  .testimonials-review {
    height: 19rem !important;
  }
}

@media (max-width: 1380px) {
  .testimonials-review {
    height: 15rem !important;
  }

  .testimonials-container {
    gap: 0.8rem;
  }

  .testimonials-text {
    margin-bottom: 1rem;
  }
}

@media (max-width: 1040px) {
  .testimonials-wrapper {
    gap: 1rem !important;
  }

  .testimonials-review {
    height: 12rem !important;
  }

  .testimonials-container h2 {
    font-size: 1.8rem !important;
  }

  .testimonials-text {
    font-size: 1.1rem !important;
  }
}

@media (max-width: 890px) {
  .testimonials-review {
    height: 10rem !important;
    padding: 1rem 1.5rem 1rem 1.5rem !important;
  }

  #load-more-button {
    border: 2px solid #000;
  }

  .testimonials-container h2 {
    font-size: 1.7rem !important;
  }

  .testimonials-text {
    font-size: 1rem !important;
    line-height: 1.1rem !important;
  }
}

@media (max-width: 720px) {
  .testimonials-review {
    height: 9.3rem !important;
    border-radius: 16px;
    padding: 0.8rem 1.2rem 0.8rem 1.2rem !important;
  }

  .testimonials-review p {
    font-size: 0.8rem !important;
  }

  .testimonials-review h1 {
    font-size: 0.9rem !important;
  }

  #brands {
    transform: scale(0.85);
  }
}

@media (max-width: 620px) {
  .testimonials {
    padding-left: 0rem !important;
    padding-right: 0rem !important;
  }

  .testimonials-review {
    height: 13rem !important;
  }

  .testimonials-review p {
    line-height: 1rem !important;
  }

  #brands {
    transform: scale(0.77);
  }
}

@media (max-width: 550px) {
  .testimonials-wrapper {
    display: block;
  }

  .testimonials-review {
    width: 65vw !important;
    margin-bottom: 0.8rem !important;
    height: 10.5rem !important;
  }

  #load-more-button {
    padding: 0.2rem 0.8rem !important;
    font-size: 1rem;
  }

  .testimonials-review h1 {
  }
}

@media (max-width: 480px) {
  .testimonials-review {
    height: 11.5rem !important;
  }
}

@media (max-width: 420px) {
  .testimonials-review {
    height: 12.5rem !important;
  }
}
</style>
