<script setup>
  import { ref, onMounted, onBeforeUnmount } from 'vue';

  import { Notyf } from 'notyf';
  import 'notyf/notyf.min.css';

  const notyf = new Notyf();

  const WEB3FORMS_ACCESS_KEY = "818e0628-b9e9-4d7a-8736-a315951a0584"

  const subject = "New message from Portfolio Contact Form";

  const name = ref("");
  const email = ref("");
  const message = ref("");

  const isLoading = ref(false);

  const submitForm = async() => {

    if(!recaptchaToken.value) {
        notyf.error("Please complete the reCAPTCHA");
        return;
    }

    isLoading.value = true;

    try {

        const response = await fetch("https://api.web3forms.com/submit", {
            method: "POST",
            headers: {
                "Content-type": "application/json",
                Accept: "application/json"
            },
            body: JSON.stringify({
                access_key: WEB3FORMS_ACCESS_KEY,
                subject: subject,
                name: name.value,
                email: email.value,
                message: message.value,
                "g-recaptcha-response": recaptchaToken.value
            })
        });

        const result = await response.json();

        if(result.success) {
            console.log(result)
            notyf.success("Message sent!");
        } else {
            notyf.error("Failed to send message");
        }

    } catch(error) {
        console.log(error);
        notyf.error("Failed to send message");

    } finally {
        isLoading.value = false;
        resetRecaptcha();
    }
}

/*recaptcha integration*/

const SITE_KEY = '6Lf-LvUsAAAAADJIFEqpdo9nRNRWk6b19F0QFXfn';

const recaptchaContainer = ref(null);
const recaptchaWidgetID = ref(null);
const recaptchaToken = ref('');

function onRecaptchaSuccess(token) {
    recaptchaToken.value = token;
}

function onRecaptchaExpired() {
    recaptchaToken.value = '';
}

function renderRecaptcha() {
    if(!window.grecaptcha) {
        console.error('reCAPTCHA not loaded');
        return;
    }

    recaptchaWidgetID.value = window.grecaptcha.render(recaptchaContainer.value, {
        sitekey: SITE_KEY,
        size: "normal",
        callback: onRecaptchaSuccess,
        'expired-callback': onRecaptchaExpired
    });
}

function resetRecaptcha() {
    if(recaptchaWidgetID.value !== null) {
        window.grecaptcha.reset(recaptchaWidgetID.value);
        recaptchaToken.value = '';
    }
}

onMounted(() => {
    const interval = setInterval(() => {
        if(window.grecaptcha && window.grecaptcha.render) {
            renderRecaptcha();
            clearInterval(interval);
        }
    }, 100);

    onBeforeUnmount(() => {
        clearInterval(interval);
    });
});
</script>

<template>
  <div id="contact">
    <div class="container-fluid">
      <div class="row text-center" id="ch">
        <p>GET IN TOUCH</p>
      </div>
      <div class="row text-center" id="cd">
        <p class="mb-5">LET'S WORK TOGETHER.</p>
      </div>
    </div>

    <div class="contact-layout-wrapper">
      <!-- Map -->
      <div id="map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d12970.694542684008!2d139.70563933327048!3d35.635771423123764!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x60188b007b69e713%3A0x1fa9f0f348e7b4bf!2sOreno%20Steak%20Ebisu!5e0!3m2!1sen!2sph!4v1775972383411!5m2!1sen!2sph"
          width="100%"
          height="656"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </div>

      <!-- Contact Info -->
      <div id="mycontact">
        <p class="contact-head">💌 EMAIL</p>
        <p class="actual-contact">andweii@gmail.com</p>
        <p class="contact-head">📞 PHONE</p>
        <p class="actual-contact">+63 123 456 7890</p>
        <p class="contact-head">📍 LOCATION</p>
        <p class="actual-contact">Japan, 〒150-0021 Tokyo, Shibuya, Ebisunishi, 1-chōme−7−１２ MKTビル 1F</p>
      </div>

      <!-- Contact Form -->
      <form id="contactform" @submit.prevent="submitForm">
        <div class="mb-3">
          <p id="cfh">CONTACT FORM</p>
          <input type="text" v-model="name" class="form-control mb-3" placeholder="Name">
          <input type="email" v-model="email" class="form-control" placeholder="Email Address">
        </div>
        <div class="mb-3">
          <textarea v-model="message" class="form-control" id="textarea" rows="5" placeholder="Message"></textarea>
        </div>

        <!-- reCAPTCHA container -->
        <div ref="recaptchaContainer" class="mb-3"></div>

        <div class="mb-3">
          <button type="submit" :disabled="isLoading">
            {{ isLoading ? "SENDING..." : "SEND MESSAGE" }}
          </button>
        </div>
      </form>
    </div>
  </div>
</template>