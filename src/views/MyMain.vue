<template>
  <div class="mymain">
    <h2>hamada</h2>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor quibusdam
      velit deserunt repellat ipsum a recusandae accusamus eius doloribus et,
      quae aliquam sit, voluptas totam! Libero voluptatem magnam deserunt eos!
    </p>
    <Content
      :students="students"
      @updateActive="changeActive()"
      :isActive="isActive"
    />
    <hr />
    <Content
      :students="students"
      @updateActive="changeActive()"
      :isActive="isActive"
    />
  </div>
</template>

<script>
import Content from "@/components/MyContent.vue";
export default {
  name: "MyContent",
  components: {
    Content,
  },
  data() {
    return {
      students: ["omar", "mohammed", "ali"],
      isActive: true,
    };
  },
  methods: {
    changeActive() {
      this.isActive = !this.isActive;
    },
  },
};
</script>
<!-- scoped & lang -->
<style scoped lang="scss">
.mymain {
  h2 {
    color: blue;
  }
  p {
    color: rgb(161, 161, 96);
  }
}
</style>
