<template>
  <section class="footer">
    <div class="footer-container">
      <h1>I am interested in getting the benefits of <span>Up Hellas</span></h1>
      <form class="form-content">
        <div class="form">
          <label for="name-surname">NAME & SURNAME</label>
          <input type="text" name="name-surname" v-model="formName" required />
          <span v-if="nameError" class="error"
            >Please enter your name and surname</span
          >
        </div>
        <div class="form">
          <label for="email">EMAIL</label>
          <input type="text" name="email" v-model="formEmail" required />
          <span v-if="emailError" class="error"
            >Please enter a valid email</span
          >
        </div>
        <div class="form">
          <label for="phone">PHONE</label>
          <input type="number" name="phone" v-model="formPhone" required />
          <span v-if="phoneError" class="error"
            >Please enter a valid phone</span
          >
        </div>
        <div class="form">
          <label for="product">PRODUCT</label>
          <input type="text" name="product" v-model="formProduct" required />
          <span v-if="productError" class="error"
            >Please enter product name</span
          >
        </div>
      </form>
      <div class="checkbox">
        <input type="checkbox" name="checkbox" id="checkbox" value="yes" />
        <p>
          Επιθυμώ να χρησιμοποιηθούν τα παραπάνω στοιχεία μου απο την Up Hellas,
          προκειμένου να ενημερωθώ για τα προιόντα της, βάσει και του Γενικού
          Κανονισμού για την Προστασία Προσωπικών Δεδομένων που ισχύει απο
          25/5/2018.
        </p>
      </div>
      <div class="form-buttons">
        <button @click="submitForm" id="send-msg-button">
          SEND US YOUR MESSAGE
        </button>
        <span>OR</span>
        <button id="meeting-button">
          <img
            id="meeting-logo"
            src="../assets/images/meeting-logo.svg"
          />SCHEDULE A MEETING
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Footer",

  data() {
    return {
      formName: "",
      formEmail: "",
      formPhone: "",
      formProduct: "",
      nameError: false,
      emailError: false,
      phoneError: false,
      productError: false,
    };
  },
  methods: {
    submitForm() {
      const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

      this.nameError = false;
      this.emailError = false;
      this.phoneError = false;
      this.productError = false;

      if (this.formName.trim() === "") {
        this.nameError = true;
      }
      if (this.formEmail.trim() === "" || !emailPattern.test(this.formEmail)) {
        this.emailError = true;
      }
      if (this.formPhone.trim() === "") {
        this.phoneError = true;
      }
      if (this.formProduct.trim() === "") {
        this.productError = true;
      }
    },
  },
};
</script>

<style>
.footer {
  background-color: #00b4d8;
  padding: 7rem 0;
  font-family: "cf_astylight", sans-serif;
}

.footer-container {
  display: grid;
  place-items: center;
}

.footer-container h1 {
  font-weight: bold;
  /* font-size: clamp(1.6rem, 2.5vw, 1.9rem); */
  font-size: 1.9rem;
}

.footer-container h1 span {
  color: #fb8b24;
}

.form-content {
  padding: 3.5rem 0rem 2rem 0;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  place-items: center;
  column-gap: 2rem;
  row-gap: 0.5rem;
}

.form {
  display: flex;
  flex-direction: column;
  height: 5rem;
}

.form label {
  font-weight: bold;
  font-family: "cf_asty_stdbold", sans-serif;
  font-size: 0.7rem;
  margin-bottom: 0.3rem;
}

.form input {
  width: 20rem;
  height: 2.5rem;
  border-radius: 24px;
  border: 1px solid #000;
  box-shadow: -3px 3px 0px #000;
  outline: none;
  padding-left: 1rem;
  background-color: #dddddd;
}

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

.form input:focus {
  box-shadow: 3px -3px 0px #000;
  background-color: #fff;
}

.checkbox {
  display: flex;
  align-items: center;
  width: 45rem;
  gap: 0.6rem;
  line-height: 1.2rem;
}

.checkbox input {
  width: 2rem;
  height: 2rem;
  outline: none;
}

.checkbox p {
  font-size: 0.75rem;
}

.form-buttons {
  margin-top: 2.2rem;
  display: flex;
  align-items: center;
  gap: 1.2rem;
  border-radius: 5px;
}

#send-msg-button,
#meeting-button {
  border-radius: 24px;
  border: 2px solid #000;
  box-shadow: -3px 3px 0px #000;
  outline: none;
  font-weight: bold;
  font-family: "cf_astylight", sans-serif;
  font-size: 0.85rem;
  cursor: pointer;
  width: 16rem;
}

#send-msg-button {
  background-color: #ffbe0b;
  padding: 0.8rem 2rem;
}

.form-buttons span {
  font-size: 0.8rem;
  font-family: "cf_astylight", sans-serif;
  font-weight: bold;
}

#meeting-logo {
  width: 1.7rem;
  height: 1.7rem;
}

#meeting-button {
  display: flex;
  align-items: center;
  gap: 0.7rem;
  padding: 0.5rem 2rem 0.5rem 1rem;
}

.error {
  color: red;
  font-size: 0.85rem;
  margin-top: 0.2rem;
}

@media (max-width: 1050px) {
  .form input {
    width: 17rem !important;
  }

  .footer-container h1 {
    font-size: 1.65rem !important;
  }

  .error {
    font-size: 0.72rem !important;
  }

  .checkbox {
    width: 40rem !important;
  }

  #send-msg-button,
  #meeting-button {
    width: 14.5rem !important;
    font-size: 0.75rem;
  }
}

@media (max-width: 700px) {
  .form input {
    width: 15rem !important;
    height: 2.2rem !important;
  }

  .footer-container h1 {
    font-size: 1.4rem !important;
  }

  .checkbox {
    width: 35rem !important;
  }
}

@media (max-width: 620px) {
  .form input {
    width: 13rem !important;
  }

  .checkbox {
    width: 30rem !important;
  }

  .footer-container h1 {
    font-size: 1.25rem !important;
  }

  .form-buttons {
    gap: 1rem !important;
  }

  #send-msg-button,
  #meeting-button {
    width: 13rem !important;
    font-size: 0.67rem;
  }

  #meeting-button {
    gap: 0.3rem !important;
    padding: 0.5rem 0.5rem 0.5rem 1.5rem !important;
  }

  .checkbox p {
    font-size: 0.7rem !important;
  }
}

@media (max-width: 490px) {
  .form input {
    width: 11rem !important;
  }

  .checkbox {
    width: 27rem !important;
  }

  .footer-container h1 {
    font-size: 1.15rem !important;
  }

  .error {
    font-size: 0.67rem !important;
  }

  #send-msg-button,
  #meeting-button {
    width: 11rem !important;
    font-size: 0.6rem;
  }

  #send-msg-button {
    padding: 0.8rem 0.5rem !important;
  }

  #meeting-button {
    padding: 0.4rem 0.4rem 0.4rem 0.85rem !important;
  }
}

@media (max-width: 450px) {
  .footer-container h1 {
    font-size: 1.05rem !important;
  }
}

@media (max-width: 430px) {
  .footer-container h1 {
    font-size: 0.9rem !important;
  }

  .form input {
    width: 9rem !important;
  }

  .checkbox {
    width: 22rem !important;
    line-height: 0.9rem !important;
  }

  #send-msg-button,
  #meeting-button {
    width: 9rem !important;
    font-size: 0.6rem;
  }

  .error {
    font-size: 0.6rem !important;
    /* background-color: red; */
    width: 8rem;
  }

  #meeting-button {
    padding: 0.3rem 0.4rem 0.3rem 0.85rem !important;
  }

  .footer {
    padding: 4rem 0 !important;
  }
}

@media (max-width: 355px) {
  .form input {
    width: 8rem !important;
    height: 2rem !important;
  }

  .checkbox {
    width: 19rem !important;
    line-height: 0.9rem !important;
  }

  .checkbox p {
    font-size: 0.67rem !important;
  }

  .footer-container h1 {
    font-size: 0.8rem !important;
  }

  #send-msg-button,
  #meeting-button {
    width: 7.5rem !important;
    font-size: 0.6rem;
    font-size: 0.5rem !important;
  }

  #meeting-button {
    padding: 0.1rem 0.3rem 0.1rem 0.85rem !important;
  }

  #send-msg-button {
    padding: 0.3rem 0.3rem 0.3rem 0.55rem !important;
  }

  #meeting-logo {
    width: 1rem !important;
  }

  .form-buttons {
    gap: 0.5rem !important;
  }
}
</style>
