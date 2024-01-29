<template>
  <div class="wrapper" id="about">
    <div class="main-container"> 
      <div class="container-one">
        <div class="profile">
          <h1>Contact info.</h1>
        </div>
        <div class="social-links">
          
            <div class="link">
              <a href="">
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
          <p>test Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
            Aut voluptatem odio impedit fugit quidem possimus laudantium 
          </p>
        </div>
        <form action="">
          <label for="">
            Name
            <input type="text">       
          </label>
          <label for="">
            Email
            <input type="email">       
          </label>
          <label for="">
            Message
            <textarea name="" id="" cols="30" rows="5"></textarea>
          </label>
          <button type="submit">SUBMIT NOW</button>
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
    background-color: #A0D4FF;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  }
  .container-one{
    background-color: #1292EE;
    padding: 2.5%;
    width:30%;
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
    }

    .container-two{
    
    width:60%;
    margin:2.5%;
  }

  .about-me{
    text-align: left;
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

  @media only screen and (max-width:950px){
    .main-container{
      width: 95%;
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