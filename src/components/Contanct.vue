<template>
  <div class="wrapper" id="about">
    <div class="main-container"> 
      <div class="container-one">
        <div class="profile">
          <h1>Contact info.</h1>
        </div>
        <div class="social-links">
          
            <div class="link">
              <a href="https://maps.app.goo.gl/M7uWujmqJBps14xk9" target="_blank">
                <img src="../assets/contact/icons8-location-48.png" alt="">
                <h2>Vauncouver</h2>
              </a>
            </div>
            <div class="link">
              <a :href="'tel:'+TEL_NUMBER">
                <img src="../assets/contact/icons8-tel-58.png" alt="">
                <h2>{{TEL_NUMBER}}</h2>
              </a>
            </div>
            <div class="link">
              <a :href="'mailto:'+EMAIL">
                <img src="../assets/contact/icons8-email-40.png" alt="">
                <h2>{{EMAIL}}</h2>
              </a>
            </div>
          
        </div>
      </div>
      <div class="container-two">
        <div class="about-me">
          <h1>Send your message</h1>
        </div>
        <form class="contactFrom" @submit.prevent="submitForm">
          <label for="name">
            Name
            <input type="text" v-model="formData.name"> 
          </label>
          <label for="email">
            Email
            <input type="email" v-model="formData.email">       
          </label>
          <label for="message">
            Message
            <textarea name="" id="" cols="30" rows="5" v-model="formData.message"></textarea>
          </label>
          <button type="submit">SUBMIT NOW</button>
          <p class="error-message">{{errorMessage}}</p>
        </form>
    </div>
    </div>
  </div>
</template>
<script>

export default {
  data(){
    return{
      TEL_NUMBER:import.meta.env.VITE_APP_PHONE_NUMBER,
      EMAIL:import.meta.env.VITE_APP_EMAIL,
      EMAIL_PASSWORD:import.meta.env.VITE_APP_EMAIL_PASSWORD,
      formData:{
        name:'',
        email:'',
        message:''
      },
      errorMessage:''
    }
  },
  methods:{
    submitForm (){
      if(this.formData.name === ""){
        this.errorMessage = "Please enter your name"
        return;
      }
      if(this.formData.email === ""){
        this.errorMessage = "Please enter your email address"
        return;
      }
      if(this.formData.message === ""){
        this.errorMessage = "Please enter your messages"
        return;
      }

      Email.send({
      Host : "smtp.elasticemail.com",
      Username : this.EMAIL,
      Password : this.EMAIL_PASSWORD,
      To : this.EMAIL,
      From : this.EMAIL,
      Subject : "You got a new contact",
      Body : `Name: ${this.formData.name}<br>Email: ${this.formData.email}<br>Message: ${this.formData.message}`
      }).then(
        message => alert(message)
      );
    }
  }
}
</script>

<style scoped>
  
  .wrapper{
    display: flex;
    justify-content: center;
  }
  img{
    height: 20px;
  }
  .main-container{
    margin-top: 30px;
    margin-bottom: 30px;
    display: flex;
    flex-direction: row;
    background-color: #cecece;
    border-radius: 25px;
    width: 70%;
    background-color: #faca9f;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  }
  .container-one{
    background-color: #eaab6c;
    padding: 2.5%;
    width:35%;
    border-radius: 25px;
  }
  .profile img{
    height: 10rem;
    border-radius: 50%;
  }

  .link a{
    text-decoration: none;
    color: #2c3e50;
    font-size: 10px;
  }

    .link img{
      height: 2rem;
      transition: transform 0.2s ease-in-out;
    }
    .link img:hover{
      transform: scale(1.3);
    }


    .container-two{
    
    width: 80%;
    margin:2.5%;
  }

  .about-me{
    text-align: center;
  }

  .contactFrom{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .contactFrom label {
  margin-bottom: 10px;
  text-align: left;
}

.contactFrom input,
.contactFrom textarea {
  width: 100%;
  padding: 8px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

.contactFrom button {
  background-color: #4e57dd;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

  .contactFrom button:hover {
    background-color: #3a3fa6;
  }

  .logos img{
    height: 2.5rem;
  }

  .button-container{
    margin-top: 5%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }

  .project-button{
    background-color: rgb(78, 87, 221);
    border-radius: 15px;
    padding: 5px;
    margin: 5px;
  }
  .project-button a{
    text-decoration: none;
    color: #fff;

  }

  .error-message{
    color: red;
  }

  @media only screen and (max-width:950px){
    .main-container{
      width: 95%;
    }
  }

  
  @media only screen and (max-width:510px){
    .main-container{
      display: flex;
      flex-direction: column;
      width: 95%;
      margin-top: 30px;
      margin-bottom: 30px;

    }
    .container-one{
    padding: 2.5%;
    width:95%;
    border-radius: 25px;
  }
  .container-two{
    
    margin: auto;
    
  }
}

  @media only screen and (max-width:400px){
    .profile img{

    height: 100%;
    width: 100%;
    border-radius: 50%;
    }
  }
</style>