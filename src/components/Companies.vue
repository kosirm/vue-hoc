<template>
  <main>
    <h3>Paper Companies</h3>
    <div v-for="(companies, i) in companies" :key="i">
      {{ companies.name }} - ${{ companies.net
      }}<button @click="setWorth(companies.id);">Set Company Value</button>
    </div>
  </main>
</template>

<script>
import mockData from "./mockData.js";
export default {
  data() {
    return {
      companies: mockData.getCompanies()
    };
  },
  methods: {
    setWorth(id) {
      mockData.setNetWorth(id);
      this.companies = mockData.getCompanies();
    }
  }
};
</script>
