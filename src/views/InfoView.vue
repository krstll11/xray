<template>
    <div class="journal-info">
      <div class="general-info">
        <h1>О Журнале</h1>
        <h1>Общая информация</h1>
        <p>
          "Новости лучевой диагностики" - первый и единственный в Республике Беларусь профессиональный журнал для врачей лучевой диагностики, рентгенолаборантов, врачей других специальностей, кому небезразличны проблемы современной рентгенологии, ультразвуковой диагностики, компьютерной и магнитно-резонансной томографии, ядерной медицины.
        </p>
        <p>
          Журнала выходит с 1998 года. На данный момент выпущено 11 печатных номеров и одно приложение (смотрите <span class="red">Архив</span>). В феврале 2001 года появилась полнотекстовая интернет-версия, а июле этого же года - <span class="red">Англоязычная интернет-версия.</span>
        </p>
    </div>
  
      <div class="editorial-board1">
        <h2>Редколлегия</h2>
        <div class="editors">
          <div class="editor">
            <img src="../assets/avatar1.png" alt="Хоружик Сергей Анатольевич" class="avatar" />
            <h4>Хоружик Сергей Анатольевич</h4>
            <p class="location">Главный редактор</p>
          </div>
          <div class="editor">
            <img src="../assets/avatar1.png" alt="Попко Юрий Федорович" class="avatar" />
            <h4>Попко Юрий Федорович</h4>
            <p class="location">Заместитель редактора</p>
          </div>
        </div>
  
        
        <div class="editorial-council">
            <h3>Редакционный совет</h3>
          <ul>
            <li><img src="../assets/avatar2.png" alt="Голуб Г. Л." class="avatar" /><p>Голуб Г. Л.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Гриньков Г. И." class="avatar" /><p>Гриньков Г. И.</p><p class='location'>Минск</p> </li>
            <li><img src="../assets/avatar2.png" alt="Зверев П. Л." class="avatar" /><p>Зверев П. Л.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Климчук Б. А." class="avatar" /><p>Климчук Б. А.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Ляхов Д. Г." class="avatar" /><p>Ляхов Д. Г.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Ляхов И. И." class="avatar" /><p>Ляхов И. И.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Михаждер М. М." class="avatar" /><p>Михаждер М. М.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Михайлов А. Н." class="avatar" /><p>Михайлов А. Н.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Очинина В. Ф." class="avatar" /><p>Очинина В. Ф.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Павлов С. М." class="avatar" /><p>Павлов С. М.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Рудкевич Е. А." class="avatar" /><p>Рудкевич Е. А.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Тихомирова Т. Е." class="avatar" /><p>Тихомирова Т. Е.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Ужко Е. А." class="avatar" /><p>Ужко Е. А.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Филипенков Н. С." class="avatar" /><p>Филипенков Н. С.</p><p class='location'>Минск</p></li>
            <li><img src="../assets/avatar2.png" alt="Чиж Г. В." class="avatar" /><p>Чиж Г. В.</p><p class='location'>Минск</p></li>
            <li class="last"><img src="../assets/avatar2.png" alt="Шилто В. В." class="avatar" /><p>Шилто В. В.</p><p class='location'>Минск</p></li>
          </ul>
        </div>
    </div>
   
    <div class="editorial-board">
    <h1 class="board-title">Редакционный совет</h1>
    <div class="board-card">
      <div class="card-image">
        <img src="../assets/avatar2.png" alt="Пользователь" />
      </div>
      <p class="card-name">Голуб Г. Д.</p>
      <p class="card-location">Минск</p>
    </div>
    <div class="pagination">
      <button class="page-button nav-button" :disabled="currentPage === 1" @click="prevPage">←</button>
      <span
        v-for="page in visiblePages"
        :key="page"
        :class="['page-button', { active: page === currentPage }]"
        @click="goToPage(page)"
      >
        {{ page }}
      </span>
      <button class="page-button nav-button" :disabled="currentPage === totalPages" @click="nextPage">→</button>
    </div>
  </div>

      
        <div class="contacts">
            <h2>Контакты</h2>
          <img src="../assets/avatar3.png" alt="Хоружик Сергей Анатольевич" class="avatar1" />
          
          <div class="address">
            <p><img src="../assets/home.png" alt="домик" class="phone-icon" />Отделение лучевой диагностики</p>
            <p class="no-icon">ГУ "РНПЦ Онкологии и медицинской<br>радиологии им. Н. Н. Александрова"</p>
            <p class="no-icon">П/о Лесное-2, 223040 Минск <br>Беларусь</p>
              
            <p><img src="../assets/phone.png" alt="Телефон" class="phone-icon" />Рабочий телефон: <a href="tel:+375173692981">+375 17 369 29 81</a></p>
          </div>
        </div>
   
    </div>
  </template>
  
  <script>
  export default {
  data() {
    return {
      currentPage: 1,
      totalPages: 16, 
    };
  },
  computed: {
    visiblePages() {
      const range = 1; 
      const pages = [];

      
      if (this.currentPage > range + 1) {
        pages.push(1);
        if (this.currentPage > range + 1) {
          pages.push("..."); 
        }
      }

     
      for (
        let i = Math.max(1, this.currentPage - range);
        i <= Math.min(this.totalPages, this.currentPage + range);
        i++
      ) {
        pages.push(i);
      }

      // Добавляем последнюю страницу, если она не в видимой зоне
      if (this.currentPage < this.totalPages - range) {
        if (this.currentPage < this.totalPages - range - 1) {
          pages.push("..."); // Указатель на пропущенные страницы
        }
        pages.push(this.totalPages);
      }

      return pages;
    },
  },
  methods: {
    goToPage(page) {
      if (page === "...") return;
      this.currentPage = page;
    },
    prevPage() {
      if (this.currentPage > 1) {
        this.currentPage--;
      }
    },
    nextPage() {
      if (this.currentPage < this.totalPages) {
        this.currentPage++;
      }
    },
  },
};
</script>
  
  <style scoped>
  
  .editor h4 {text-decoration: underline; color:#B90B0B}
  .no-icon{padding-left:50px;}
  .red{color:#B90B0B;text-decoration: underline}
h1{ font-size:36px;font-weight: bolder;}
h2{ font-size:36px;font-weight: bolder;}
h3{ font-size:36px;font-weight: bolder;}
h4{ text-decoration: underline; color:#B90B0B}
.general-info h1{padding-top: 15px;padding-bottom: 15px;}
  .avatar1 img {
    
    width: 576px;
    height: 576px;}
  .location{color: rgb(129, 129, 129);
  font-size:16px}
  .contacts h2{
    padding-bottom: 30px;}


  .editorial-council{padding-top: 30px;display: block;}
  .editorial-board{display: none;}
  .journal-info {
    font-family: Arial, sans-serif;
    padding: 20px;
  }
  
  .general-info {
    margin-bottom: 20px;
    
  }
  .general-info p {
      text-align: left;
  }
  .general-info h1 {
      text-align: left;
  }
  .editors {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
  }
  .editorial-council h3{
    text-align: center; 
    padding-bottom: 30px;}
  .editorial-council ul {
    list-style: none;
  padding: 0;
  display: grid;
  grid-template-columns: repeat(5, 1fr); 
  gap: 20px;
  text-align: center;
  }
  .editorial-council ul .last{
  grid-column: span 5; 
}
  .editor {
    text-align: center;
    max-width: 150px;
  }
  
  .avatar {
    width: 80px;
    height: 80px;
    margin: 0 auto 10px;
    object-fit: cover;
  }
  
  .contacts {
    padding-top: 30px;
    margin:auto;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .address p{
    line-height: 30px;
    text-align: start;
  }
  
 
  
  .contacts a {
    color: #007bff;
    text-decoration: none;
  }
  
  @media (max-width: 768px) {
    .editors {
      flex-direction: column;
      align-items: center;
    }
  
    .editorial-council ul {
      grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    }
  }
  
  @media (max-width: 480px) {
    .editorial-board {
      display: block;
  text-align: center;
  padding: 20px;
  border-radius: 10px;
  background-color: #f9f9f9;
  max-width: 400px;
  margin: 0 auto;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
.editorial-council{display: none;}
.board-title {
  font-size: 18px;
  margin-bottom: 20px;
  font-weight: bold;
}
.board-card {
  text-align: center;
  padding: 20px;
  background-color: white;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}
.card-image img {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-bottom: 10px;
}
.card-name {
  font-size: 16px;
  font-weight: bold;
  margin: 5px 0;
}
.card-location {
  font-size: 14px;
  color: gray;
  margin: 0;
}
.pagination {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5px;
  margin-top: 20px;
  background-color: #555;
  border-radius: 8px;
  padding: 5px 10px;
}
.page-button {
  padding: 5px 10px;
  border: none;
  background-color: transparent;
  color: white;
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
}
.page-button.active {
  text-decoration: underline;
  color: #d32f2f;
}
.page-button.nav-button {
  background-color: #d32f2f;
  border-radius: 4px;
  color: white;
}
.page-button.nav-button:disabled {
  background-color: #999;
  cursor: not-allowed;
}
.ellipsis {
  color: white;
}

.card {
  display: inline-block;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 20px;
  max-width: 200px;
  text-align: center;
}

.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  margin-bottom: 10px;
}

.pagination-controls {
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.prev-button, .next-button {
  padding: 5px 10px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.prev-button:disabled, .next-button:disabled {
  background-color: #ccc;
  cursor: not-allowed;
}
  }
  </style>
  