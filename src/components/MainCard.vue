<template lang="">
  <div class="main-container"> 
    <div class="container-one">
      <div class="profile">
        <img src="../assets/IMG_1040.png" alt="">
        <h3>Name here</h3>
        <p>Software Developer</p>
      </div>
      <div class="social-links">
        
          <div class="link">
            <a href="">
              <img src="../assets/icons8-github-94.png" alt="">
              <h2>GitHub</h2>
            </a>
          </div>
          <div class="link">
            <a href="">
              <img src="../assets/icons8-linkedin-96.png" alt="">
              <h2>LinkedIn</h2>
            </a>
          </div>

        
      </div>
    </div>
    <div class="container-two">
      <div class="about-me">
        <h1>About Me</h1>
        <p>test Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
          Aut voluptatem odio impedit fugit quidem possimus laudantium 
          corporis reprehenderit facere dolorum quasi, eligendi earum.
           Qui adipisci cum, ipsum distinctio iure doloribus.
        </p>
      </div>
      <div class="technology-section">
      <h1>Technologies Studied</h1>
      <img src="../assets/icons8-github-94.png" alt="">
      <img src="../assets/icons8-github-94.png" alt="">
      <img src="../assets/icons8-github-94.png" alt="">
      <img src="../assets/icons8-github-94.png" alt="">
      <img src="../assets/icons8-github-94.png" alt="">
      <img src="../assets/icons8-github-94.png" alt="">
    </div>
    <div class="button-container">
      <div class="project-button">
        <a href="">My projects</a>
        <div>
          <a href="">My Resume</a>
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
  img{
    height: 20px;
  }
  .main-container{
    display: flex;
    flex-direction: row;
    background-color: grey;
    border-radius: 25px;
  }
  .container-one{
    background-color: rgb(227, 147, 213);
    padding: 2.5%;
    width:40%;
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
    background-color: blueviolet;
    width:60%;
    margin:2.5%;
  }

  .about-me{

  }

</style>