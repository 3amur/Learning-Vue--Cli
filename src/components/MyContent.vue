<template>
  <div class="my-content">
    <ul>
      <li v-for="(student, i) in students" :key="i">{{ student }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["students"],
};
</script>

<style scoped lang="scss">
.my-content {
  ul {
    list-style: none;
  }
  li {
    display: flex;
    justify-content: space-between;
    list-style: none;
    align-items: center;
  }
}
</style>
