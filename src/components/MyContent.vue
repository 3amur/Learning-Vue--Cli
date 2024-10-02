<template>
  <div class="my-content">
    <ul>
      <li v-for="(student, i) in students" :key="i">{{ student }}</li>
    </ul>
    <button @click="deleteSt">Change Data</button>
    <h2>Activation is {{ isActive }}</h2>
    <button @click="changeActive()">Change Activation</button>
  </div>
</template>

<script>
export default {
  // props: ["students", "isActive"],
  props: {
    students: {
      type: Array,
      required: true,
    },
    isActive: {
      type: Boolean,
    },
  },
  data() {
    return {
      myStudents: this.students,
    };
  },
  methods: {
    deleteSt() {
      this.myStudents.shift();
    },
    changeActive() {
      this.$emit("updateActive");
    },
  },
};
</script>

<style scoped lang="scss">
.my-content {
  ul {
    display: flex;
    justify-content: space-around;

    list-style: none;
    gap: 20px;
    align-items: center;
  }
  li {
    justify-content: space-around;
    align-items: center;
  }
}
</style>
