<template>
  <div class="container">
    <img src="../assets/logo 1.png" class="logo" alt="Logo" v-on:click="this.$router.push('/')">
    
    <div class="navbar-container">
      <div class="navbar">
        <h1 v-on:click="this.$router.push('/info')">О журнале</h1>
        <h1 v-on:click="this.$router.push('/archive')">Архив</h1>
        <h1 class="active">База изображений</h1>
        <h1 class="active">Авторам</h1>
        <h1 class="active">Документы</h1>
        <div class="menu">
          <img src="../assets/menu.png" alt="Menu">
        </div>
        </div>
        <div class="under-headers">
        <div class="text-line">
          <h1>Поиск на сайте...</h1>
          <h1>🔍︎</h1>
          </div>
          <div class="text-line1">
          <img src="../assets/lang.png" alt="Language Switcher">
        </div>
      
      </div>


      </div>
    </div>
    

</template>

<style scoped>

.logo{cursor: pointer;}
.container {
  padding: 20px;
  display: flex;
  flex-direction: row;

  background-color: #df1717;
  font-size: 24px;
  color: white;
}
.navbar-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.navbar {
  display: flex;
  flex-direction: row;
  justify-content:space-evenly;
  align-items: center;
  margin-bottom: 10px;
  
}

.navbar h1 {
  margin: 0;
  cursor: pointer;
}


.menu img {
  display: block;
  height: 48px;
  width: 85px;
  cursor: pointer;
  margin-left: auto;
}


.under-headers {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin-right: 35px;
}

.text-line {
  height:35px;
  justify-content: space-between;
  display: flex;
  flex-direction: row;
  background-color: aliceblue;
  color: black;
  padding: 5px 10px;
  border-radius: 4px;
  padding-top: 10px;
  cursor: pointer;
  width: 70%;
}
.text-line h1{font-size:24px;color:grey}

.text-line1 img {
  display: block;
  height: 56px;
  width: 56px;
  cursor: pointer;
  margin-left:40px
}
@media screen and (max-width: 720px) {
 .container{font-size: 20px;}
  .active {
    display: none;
  }
  .text-line h1{font-size: 20px;padding-top:5px}
  .logo{
    margin-top: auto;
    margin-bottom: auto;
    width: 55px;
    height: 55px;
  }
  .text-line1 img {
  display: block;
  height: 28px;
  width: 28px;
  cursor: pointer;
  margin-left:40px
}
.menu img{
  height: 28px;
  width: 48px;
}
.text-line{
  margin-left: 20px;
  font-size:14px;
  width: 60%;
}
}
</style>
