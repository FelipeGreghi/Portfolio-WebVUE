<template>
    <div class="contact-container">
      <div class="left-side">
        <h1>
          Let's chat.<br />
          Tell me about your project.
        </h1>
        <p>Let's create something together ✌️</p>
        <a href="mailto:felipegreghi25@gmail.com" class="email-link">
          Mail me at <strong>felipegreghi25@gmail.com</strong>
        </a>
      </div>
  
      <div class="right-side">
        <form @submit.prevent="sendMessage">
          <h3>Send me a message 🚀</h3>
          <input
            type="text"
            v-model="formData.name"
            placeholder="Full name*"
            required
          />
          <input
            type="email"
            v-model="formData.email"
            placeholder="Email address*"
            required
          />
          <input type="text" v-model="formData.subject" placeholder="Subject" />
          <textarea
            v-model="formData.message"
            placeholder="Tell us more about your project*"
            required
          ></textarea>
          <button type="submit">Send message</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
    export default {
    data() {
      return {
        formData: {
          name: "",
          email: "",
          subject: "",
          message: ""
        }
      };
    },
    methods: {
      sendMessage() {
        const { name, email, subject, message } = this.formData;
        const formattedMessage = `*Contact Form Submission*\nName: ${name}\nE-mail: ${email}\n\nSubject: ${subject}\n\nDescription of the project:\n*------------------------------------*\n${message}\n*------------------------------------*`;
        const whatsappUrl = `https://wa.me/5516991609156?text=${encodeURIComponent(formattedMessage)}`;
        window.open(whatsappUrl, '_blank');
      }
    }
  };
  </script>
  
  <style scoped>
  .contact-container {
    display: flex;
    justify-content: space-between;
    max-width: 70%;
    padding: 5%;
    background-color: #fff;
    border-radius: 15px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    font-family: Arial, sans-serif;
  }
  
  .left-side {
    width: 40%;
    border-right: 1px solid #ddd;
  }
  
  .left-side h1 {
    font-size: 2.7em;
    margin-bottom: 20px;
  }
  
  .left-side p {
    font-size: 16px;
    margin-bottom: 20px;
  }
  
  .email-link {
    font-size: 16px;
    color: #555;
    text-decoration: none;
  }
  
  .right-side {
    width: 50%;
    padding: 20px;
    border-radius: 10px;
  }
  
  form h3 {
    font-size: 30px;
    margin-bottom: 20px;
  }

  input, textarea {
    width: 100%;
    padding: 5px;
    margin-bottom: 15px;
    border: 1px solid #ddd;
    border-radius: 5px;
    font-size: 14px;
  }
  
  button {
    background-color: #46BABE;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #509295;
  }
</style>
