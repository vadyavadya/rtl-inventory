<script setup lang="ts">
import Person from "@/components/Person.vue";
import Footer from "@/components/Footer.vue"

</script>

<template>
  <main class="main">
    <div class="main-container">
      <Person />
    </div>
    <Footer />
  </main>


</template>

<style scoped lang="scss">
.main {
  max-width: 870px;
  margin: 0 auto;
  padding: 32px 42px;
}

.main-container {
  margin-bottom: 24px;
  display: flex;
  gap: 24px;
}
</style>
