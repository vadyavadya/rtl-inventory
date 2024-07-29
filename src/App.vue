<script setup lang="ts">
import Person from "@/components/Person.vue";
import Footer from "@/components/Footer.vue";
import Inventory from "@/components/Inventory.vue";

</script>

<template>
  <main class="main">
    <div class="main-container">
      <Person />
      <Inventory class="inventory"/>
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

.inventory {
  flex: 1 0 auto;
}
</style>
