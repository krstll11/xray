<template>
  <div class="archive">
    <h1 class="archive-title">Архив</h1>
    <div class="pagination">
      <button class="page-button nav-button" :disabled="currentPage === 1" @click="prevPage">←</button>
      <div
        v-for="page in visiblePages"
        :key="page"
        :class="['page-button', { active: page === currentPage }]"
        @click="goToPage(page)"
      >
        {{ page }}
      </div>
      <div v-if="currentPage < totalPages - 2" class="ellipsis">...</div>
      <div
        v-if="currentPage < totalPages - 1"
        :class="['page-button', { active: totalPages === currentPage }]"
        @click="goToPage(totalPages)"
      >
        {{ totalPages }}
      </div>
      <button class="page-button nav-button" :disabled="currentPage === totalPages" @click="nextPage">→</button>
    </div>
    <div class="archive-grid">
      <div v-for="issue in currentIssues" :key="issue.id" class="archive-item">
        <img :src="issue.image" alt="Архив" class="archive-image" />
        <p class="archive-title">{{ issue.title }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentPage: 1,
      issuesPerPage: 12, // Значение по умолчанию
      issues: [],
    };
  },
  computed: {
    totalPages() {
      return Math.ceil(this.issues.length / this.issuesPerPage);
    },
    visiblePages() {
      const range = 3;
      const pages = [];
      for (let i = 1; i <= Math.min(range, this.totalPages); i++) {
        pages.push(i);
      }
      if (this.currentPage > range) {
        pages.splice(1, 0, "...");
      }
      return pages;
    },
    currentIssues() {
      const start = (this.currentPage - 1) * this.issuesPerPage;
      const end = start + this.issuesPerPage;
      return this.issues.slice(start, end);
    },
  },
  created() {
    // Инициализация списка выпусков
    for (let i = 1; i <= 48; i++) {
      this.issues.push({
        id: i,
        title: `Номер ${i}, 2000`,
        image: this.getRandomImage(),
      });
    }
    // Установка количества элементов на странице
    this.updateIssuesPerPage();
    window.addEventListener("resize", this.updateIssuesPerPage);
  },
  beforeDestroy() {
    // Удаление обработчика resize
    window.removeEventListener("resize", this.updateIssuesPerPage);
  },
  methods: {
    updateIssuesPerPage() {
      this.issuesPerPage = window.innerWidth <= 720 ? 4 : 12;
    },
    getRandomImage() {
      const randomIndex = Math.floor(Math.random() * 12) + 1;
      return new URL(`../assets/archive${randomIndex}.png`, import.meta.url).href;
    },
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
.archive {
  text-align: center;
  padding: 20px;
}
.archive-title {
  margin-bottom: 20px;
}
.pagination {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  margin-bottom: 20px;
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
.archive-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  flex: 3;
}
.archive-item {
  text-align: center;
}
.archive-image {
  max-width: 100%;
  height: auto;
  display: block;
  margin: 0 auto 10px;
}
h1 {
  font-weight: bolder;
  font-size: 48px;
}
p {
  font-weight: bolder;
  font-size: 24px;
}
@media screen and (max-width: 720px) {
  h1 {
    font-weight: bolder;
    font-size: 36px;
  }
  p {
    font-weight: bolder;
    font-size: 24px;
  }
  .archive-grid {
    grid-template-columns: repeat(1, 1fr);
    gap: 20px;
  }
}
</style>
