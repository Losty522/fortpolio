<template>
  <header class="main-container" id="home">
    <nav class="icon"><a href="#home"><img src="../assets/page.jpg" alt=""></a></nav>
    <nav><a href="#home">HOME</a></nav>
    <nav><a href="#about">ABOUT</a></nav>
    <nav><a href="#project">PROJECT</a></nav>
    <nav><a href="#contact">CONTACT</a></nav>
  </header>
</template>
<script>
export default {
  
}
</script>
<style scoped>
  .icon{
    margin-right: auto;
  }
  .icon img{
    margin-top: 2px;
    height: 2rem;
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

</style>