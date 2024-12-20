<template>
    <footer class="footer">
      <div class="footer-top">
        <div class="footer-left"><h1>Проект создан</h1><h1>20.02.01</h1></div>
        <div class="footer-center"><h1>Обновлено</h1><h1>20.02.01</h1></div>
        <div class="footer-right"><h1>Хостинг</h1><h1 class="under">Tut.by</h1></div>
      </div>
      <div class="footer-bottom">
        <div class="footer-line"></div>
        <div class="footer-credit">
          Разработка и дизайн © Сергей А. Хоружик, 2001-2014
        </div>
      </div>
    </footer>
  </template>
  
  <script>

  </script>
  
  <style scoped>
  .under{text-decoration: underline;}
  .footer {
    font-size: 24px;
    background-color: #808080; /* серый цвет */
    height: 120px;
    display: flex;
    flex-direction: column;
    flex-wrap:wrap;
    justify-content: space-between;
    padding: 20px;
    color: white;
    font-family: Arial, sans-serif;
  }
  
  .footer-top {
    display: flex;
    justify-content: space-between;
  }
  
  .footer-bottom {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
  }
  
  .footer-info {
    display: flex;
    justify-content: space-between;
    width: 100%;
    margin-bottom: 10px;
  }
  
  .footer-date,
  .footer-link {
    margin: 0;
  }
  
  .footer-link {
    color: white;
    text-decoration: underline;
  }
  
  .footer-line {
    width: 95%;
    height: 2px;
    background-color: white;
    margin: auto;

  }
  
  .footer-credit {
    padding-top: 20px;
    align-self: flex-start;
    font-size: 12px;
  }
  @media screen and (max-width: 480px) {
    .footer-top {display:grid; grid-template-columns: repeat(2, 1fr);
    
  }
  .footer-right{margin:auto;}
}

.footer-credit{padding-top:0px}
    .footer-right{  grid-column: span 2}
  </style>
  