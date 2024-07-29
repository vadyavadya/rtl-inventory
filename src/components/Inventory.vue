<template>
  <div class="card inventory">
    <div class="line" v-for="line in slots">
      <div class="slot" v-for="slot in line">

      </div>
    </div>
    <draggable v-model="list" item-key="id" :swap='true' swap-class="highlighted"> 
      <template #item="{ element }">
        <div class="slot">{{ element.name }}</div>
      </template>
      </draggable>
  </div>
</template>

<script setup lang="ts">
import draggable from 'vuedraggable';
import { ref } from 'vue';
import type { Ref } from 'vue';

type List = {
  name: string,
  id: number
}

const list: Ref<Array<List>> = ref([
  {
    name: 'Joao',
    id: 1
  },
  {
    name: 'Jean',
    id: 2
  },
  {
    name: 'Johanna',
    id: 3
  },
  {
    name: 'Juan',
    id: 4
  }
])

let slots = Array(5).fill(Array(5).fill(null));

</script>

<style scoped lang="scss">
.card {}

.slot {
  border: 0.5px solid #4d4d4d;
  width: 105px;
  height: 100px;
}

.card {
  overflow: hidden;
}

.line {
  display: flex;
  margin: 0 -0.5px;

  &:first-child {
    margin-top: -0.5px;
  }

  &:last-child {
    margin-bottom: -0.5px;
  }
}
</style>