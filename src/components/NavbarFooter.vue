<template>
  <footer class="main-container" id="home">
    <nav class="name">Kenshiro Yasu</nav>
    <nav><a href="#home">HOME</a></nav>
    <nav><a href="#about">ABOUT</a></nav>
    <nav><a href="#project">PROJECT</a></nav>
    <nav><a href="#contact">CONTACT</a></nav>
  </footer>
</template>
<script>
export default {
  
}
</script>
<style scoped>
  .name{
    margin-right: auto;
    padding-left: 10px;
    color: #fff;
    margin-top: 2px;
    border-radius: 50%;
  }
  .main-container {
    height: 3rem;
    background-color: rgb(72, 72, 72);
    display: flex;
    justify-items: center;
    align-items: center;
    justify-content: flex-end;
    padding-right: 20px;
  }
  .main-container a{
    text-decoration: none;
    color: #fff;
    margin-left: 20px;
  }
  .main-container a:hover{
    
    color: #ef0000;
    
  }
  @media only screen and (max-width:400px){
    .main-container{
      font-size: 10px;
    }
  }

</style>