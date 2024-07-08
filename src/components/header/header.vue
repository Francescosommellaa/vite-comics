<script setup>
const app = Vue.createApp({
  data() {
    return {
      menuItems: [
        { label: 'Characters', active: false },
        { label: 'Comics', active: true }, 
        { label: 'Movies', active: true }, 
        { label: 'TV', active: true }, 
        { label: 'Games', active: true }, 
        { label: 'Collectibles', active: true }, 
        { label: 'Videos', active: true }, 
        { label: 'Fans', active: true }, 
        { label: 'News', active: true },
        { label: 'Shop', active: true },
      ],
    };
  },
  methods: {
    toggleActive(index) {
      this.menuItems.forEach((item, i) => {
        item.active = i === index ? !item.active : false;
      });
    },
  },
});

</script>

<template>
  <div id="app" class="container">
    <img src="../..//assets/img/dc-logo.png" alt="logo DC Header">
    <ul>
    <li v-for="(item, index) in menuItems" :key="index" @click="toggleActive(index)">
      {{ item.label }}
    </li>
  </ul>
  </div>
</template>

<style scoped>

</style>