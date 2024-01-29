<template lang="">
  <div class="wrapper" id="about">
    <div class="main-container"> 
      <div class="container-one">
        <div class="profile">
          <img src="../assets/IMG_1040.png" alt="">
          <h3>Kenshiro Yasu</h3>
          <p>Front-End Developer</p>
        </div>
        <div class="social-links">
          
            <div class="link">
              <a href="https://github.com/Losty522" target="_blank">
                <img src="../assets/icons8-github-94.png" alt="">
                <h2>GitHub</h2>
              </a>
            </div>
            <div class="link">
              <a href="https://www.linkedin.com/in/kenshiro-yasu-62a78527a/" target="_blank">
                <img src="../assets/icons8-linkedin-96.png" alt="">
                <h2>LinkedIn</h2>
              </a>
            </div>

          
        </div>
      </div>
      <div class="container-two">
        <div class="about-me">
          <h1>About Me</h1>
          <p>
            Passionate gamer turned engineer with a knack for tinkering since elementary school.
             From Embedded Pachinko systems to customer support, I've consistently leveraged programming for efficiency.
              Now, transitioning to web development, my diverse experiences and programming skills make me a versatile professional
               ready to tackle challenges in this field. Let's connect and explore the possibilities together.
          </p>
        </div>
      <div class="technology-section">
        <h1>Technologies Studied</h1>
        <div class="logos">
        <div class="inner-logos">
          <img src="/skills/icons8-typescript-48.png" alt="TypeScript">
          <!-- <img src="../assets/skills/icons8-javascript-48.png" alt="">
          <img src="../assets/skills/icons8-react-100.png" alt="">
          <img src="../assets/skills/icons8-nextjs-48.png" alt="">
          <img src="../assets/skills/icons8-vue-js-48.png" alt=""> -->

        </div>
        <div>
          <!-- <img src="../assets/skills/icons8-jquery-is-a-javascript-library-designed-to-simplify-html-48.png" alt="">
          <img src="../assets/skills/icons8-html-48.png" alt="">
          <img src="../assets/skills/icons8-css-48.png" alt="">
          <img src="../assets/skills/icons8-mongodb-48.png" alt="">
          <img src="../assets/skills/icons8-nodejs-48.png" alt=""> -->
        </div>
        </div>
      </div>
      <div class="button-container">
        <div class="project-button">
          <a href="#project">My projects</a>
        </div>
        <div class="project-button">
          <a href="https://drive.google.com/file/d/12uAxnlOGP3UcFBR4E6CVvV96MvqTjPr5/view?usp=sharing" target="_blank">My Resume</a>
        </div>      
      </div>
    </div>
    </div>
  </div>

</template>
<script>
export default {
  
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
    background-color: #dcdf9a;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  }
  .container-one{
    background-color: #ede492;
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
    margin-left: 7px;
    margin-right: 7px;
  }

  .button-container{
    margin-top: 5%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }

  .project-button{
    background-color: rgb(119, 113, 226);
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