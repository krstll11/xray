<template>
    <div class="page-wrapper">
      <div class="alert-banner">
        <h3>Внимание посетителей сайта</h3>
        <p>
          В связи с прекращением выхода журнала "Новости лучевой диагностики" сайт обновляется редко. 
          Доступны архив номеров, а также разнообразные образовательные материалы
        </p>
        <div class="alert-icon">!</div>
      </div>
  
  
      <div class="current-issue">
        <h2>Номер 1/2004 (Текущий)</h2>
      </div>

  <div class="content-block">
    <div class="image-container">
        <h3>Рентгенология</h3>
      <img src="../assets/xray.png" alt="xray" class="image" />
    </div>

    <div class="text-container">

      <div class="text-box">
        <p class="text-main">
          Закономерности между ангиографической семиотикой почечно-клеточного рака и морфологическим строением опухоли
        </p>
        <p class="text-author">Акинфеев В.В.</p>
      </div>

      <div class="text-box">
        <p class="text-main">
          Первый опыт использования многосрезовой компьютерной томографии в Республике Беларусь
        </p>
        <p class="text-author">Хоружик С.А., Дзюбан В.П.</p>
      </div>
      
    </div>
    
</div>

<div class="content-block">
    <div class="image-container">
        <h3>Ультразвуковая</h3>
        <h3>диагностика</h3>
      <img src="../assets/supersonic.png" alt="ss" />
    </div>

    <div class="text-container">

      <div class="text-box">
        <p class="text-main">
            Скрининговые ультразвуковых исследований щитовидной железы в Брянской области
        </p>
        <p class="text-author">Нефёдов В.А.</p>
      </div>

      <div class="text-box">
        <p class="text-main">
            Значение ультразвуковой томографии в диагностике и малоинвазивном лечении простой кисты почки
        </p>
        <p class="text-author">Нечипоренко Н.А., Нечипоренко А.Н., Балла А.А.</p>
      </div>
      
    </div>
    
</div>
<div class="content-block">
    <div class="image-container">
        <h3>Магнитно-резонансная</h3>
        <h3>томография</h3>
      <img src="../assets/mrt.png" alt="mrt" class="image" />
    </div>

    <div class="text-container">

      <div class="text-box">
        <p class="text-main">
          Комплекс для рено-графического исследования и программное обеспечение обработки рено-графической кривой        </p>
        <p class="text-author">Сакович Р.А., Ситник А.А.</p>
      </div>
      
    </div>
    
</div>
<div class="content-block">
    <div class="image-container">
        <h3>Ядерная медицина</h3>
      <img src="../assets/nuclear.png" alt="nuclear" class="image" />
    </div>

    <div class="text-container">

      <div class="text-box">
        <p class="text-main">
          МРТ в диагностике посттравматических изменений коленного сустава        </p>
        <p class="text-author">Терехов В.И., Климахович В.В., Харченко А.С.</p>
      </div>
      
    </div>
    
</div>
<div class="content-block">
    <div class="image-container">
        <h3>Рентгенология</h3>
      <img src="../assets/poet.png" alt="poet" class="image" />
    </div>

    <div class="text-container">

      <div class="text-box">
        <p class="text-main">
          Комплекс для рено-графического исследования и программное обеспечение обработки рено-графической кривой        </p>
        <p class="text-author">Терехов В.И., Климахович В.В., Харченко А.С.</p>
      </div>
      
    </div>
    
</div>
</div>

  </template>
  
  <style scoped>

  .page-wrapper {
    font-family: Arial, sans-serif;
    max-width: 69%;
    margin: 0 auto;
    padding: 20px;
    background-color: #ffffff;
  }
  
 
  .alert-banner {
    text-align: center;
    background-color: #FEEDED;
    border: 2px solid #df1717;
    padding: 10px;
    margin-bottom: 20px;
    position: relative;
  }
  
  .alert-banner h3 {
    font-size:32px;
    text-decoration: underline;
    color: #df1717;
    font-weight: bold;
    margin: 0;
  }
  
  .alert-banner p {
    margin: 5px 0;
    color: #333;
  }
  
  .alert-icon {
    position: absolute;
    right: 10px;
    top: 10px;
    font-size: 48px;
    color: #df1717;
  }
  
 
  .current-issue {
    text-align: center;
    background-color: #df1717;
    color: white;
    padding: 10px;
    font-size: 20px;
    margin-bottom: 20px;
    border-radius: 8px;
  }
  
 .content-block {
  display: flex;
  
  align-items: flex-start;
  gap: 20px;
  padding: 20px;
  background-color: #ffffff;
  border-radius: 10px;
}

.image-container img {
  width: 282px;
  height: 282px;
  border-radius: 8px;
  object-fit: cover;
}
.image-container h3{
  text-align: center;
font-size: 24px;
font-weight: bolder;}
.text-container {
  display: flex;
  flex-direction: column;
  gap: 15px;
  width: 70%;
}

.text-box {
text-align: center;
  background-color: white;
  padding: 10px 15px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.text-main {
  font-size: 18px;
  color: #000;
  margin: 0 0 5px 0;
}

.text-author {
  font-size: 14px;
  color: #8f8f8f;
  text-align: right;
  margin: 0;
}
@media screen and (max-width: 720px) {

  .page-wrapper {

    margin:auto;
    font-family: Arial, sans-serif;
    width: 100%;
    background-color: #ffffff;
  }
  .content-block {
    margin:auto;
    flex-wrap: wrap;
    padding:0;
}
.image-container img{
  width: 100%;
  margin:auto;
}

.text-container{
  margin:auto;
  padding: 0;
  width: 100%;
}
}
  </style>
  