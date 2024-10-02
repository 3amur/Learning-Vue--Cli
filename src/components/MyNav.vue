<template>
  <div class="my-nav">
    <div class="ivon">Icon</div>
    <div class="logo">{{ logo }}</div>
    <div class="links">
      <ul>
        <li v-for="link in links" :key="link">{{ link }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
// export component to use in any file ou want
export default {
  data() {
    return {
      logo: "My logo",
      links: ["link1", "link2"],
    };
  },
};
</script>

<style scoped>
.my-nav {
  padding: 20;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
ul {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  list-style: none;
}
</style>
