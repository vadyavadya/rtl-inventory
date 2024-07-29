<template>
  <div class="card">
    <div class="img-container">
      <img src='/Img.jpg' alt="">
    </div>
    <div class="information">
      <h2 class="title-skeleton"></h2>
      <p class="text-skeleton" :style="{ 'width': '81.5%' }"></p>
      <p class="text-skeleton"></p>
      <p class="text-skeleton" :style="{ 'width': '90%' }"></p>
      <p class="text-skeleton" :style="{ 'width': '85%' }"></p>
      <p class="text-skeleton" :style="{ 'width': '80%' }"></p>
      <p class="text-skeleton" :style="{ 'width': '45%' }"></p>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
.card {
  padding: 18px 14px 24px 14px;
}

.img-container {
  margin: 0 auto;
  overflow: hidden;
  border-radius: 8px;
  width: 208px;
  margin-bottom: 12px;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    filter: blur(5px);
  }
}

.information {
  padding: 0 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.title-skeleton {
  margin-bottom: 1.5rem;
}

.text-skeleton {
  &:not(:last-child) {
    margin-bottom: 1rem;
  }
}
</style>