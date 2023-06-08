<template>
  <div class="container bg-black pt-5 py-5 my-5">
    <div class="row text-white">
      <div class="col-sm-6">
        <Title label="Réservations" centered />
        <p class="mt-4">
          Un afterwork, un anniversaire, un séminaire ou quelque chose à fêter ? Nous vous proposons de réserver sans frais un espace afin d’organiser votre évènement chez Tic & Tac Bar. Pour plus d’informations, n’hésitez pas à nous contacter (en précisant la date et l’heure souhaitées ainsi que le nombre d’invités).
        </p>
      </div>

      <div class="col-sm-6">
        <form action="" class="formFields" @submit.prevent="sendEmail">
          <div class="name-field">
            <div class="field">
              <input type="text" v-model="firstName" placeholder="First Name" />
            </div>
            <div class="field">
              <input type="text" v-model="subject" placeholder="Subject of message" />
            </div>
          </div>
      
          <div class="emaill-field field">
            <input type="email" v-model="email" placeholder="Enter your Email" />
          </div>
      
          <div class="field">
            <textarea  type="textarea" v-model="message" placeholder="Enter Message" />
          </div>
          <div class="submimtbutton field">
            <button type="submit">SUBMIT</button>
          </div>
        </form>
          </div>
        </div>
      </div>
  
  <!-- form -->
</template>

<script>
import { reactive, toRefs, watch } from 'vue'
import Title from '@/components/UI/Title.vue'
import { Email } from '@/assets/smtp/smtp.js'

export default {
  name:'Contact',
  components: { Title },
  data() {
    return {
      firstName: "name test",
      email: "",
      subject: "subject test",
      message: "test smtp",
    }
  },
  methods: {
    sendEmail() {
      Email.send({
        Host : "smtp.elasticemail.com",
        Username : "nils.vainui@gmail.com",
        Password : "E7AC50FE16DFF9812A2E20D501E42306BBC1",
        To: "nils.vainui@gmail.com",
        From: "nilsdraw@gmail.com",
        Name: this.name,
        Subject: this.subject,
        Body: this.message
      }).then((message) => alert(message))
    }
  }
}
</script>

<style scoped>
.textYellowNoDeco{
  color: #F6A424;
  text-decoration: none;
}
.textJustify{
    text-align: justify;
  text-justify: inter-word;
}
.email{
    margin-left: 15%;
}

.contact-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  background-color: #fff;
  height: 70vh;
  width: 60%;
  margin: 10px auto;
  padding: 10%;
  color: black;
}
.field {
  margin: 10px 0;
}
input,
textarea {
  height: 50px;
  width: 100%;
  margin: 20px;
  border-top: none;
  border-right: none;
  border-left: none;
  outline: none;
}
.submitbutton button {
  height: 50px;
  width: 200px;;
  margin: 0 auto;
  text-align: center;
  font-weight: 300;
  border-radius: 30px;
  border: 2px solid rgb(133,133,133);
  display: flex;
  justify-content: center;
}
.contact-title {
  text-align: center;
}
</style>