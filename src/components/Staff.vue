<template>
  <main>
    <h3>Staff List</h3>
    <div v-for="(staff, i) in staffList" :key="i">
      {{ staff.name }}: {{ staff.awards }} Salesman of the year Award 🎉
      <button @click="increaseAwards(staff.id);">+</button>
      <button @click="decreaseAwards(staff.id);">-</button>
    </div>
  </main>
</template>

<script>
import mockData from "./mockData.js";
export default {
  data() {
    return {
      staffList: mockData.getStaff()
    };
  },
  methods: {
    increaseAwards(id) {
      mockData.increaseAward(id);
      this.staffList = mockData.getStaff();
    },
    decreaseAwards(id) {
      mockData.decreaseAward(id);
      this.staffList = mockData.getStaff();
    }
  }
};
</script>
