<script setup>
import { ref } from 'vue'

const showModal = ref(false);


</script>

<template>
  <main>
    <div v-if="showModal" class="overlay flex items-center">
      <div class="bg-white rounded-md p-10 flex flex-col w-1/3">
        <textarea class="border mb-3" name="note" id="note" cols="30" rows="10"></textarea>
        <button class="bg-blue-400 hover:bg-blue-500 text-white mb-3 cursor-pointer">Add note</button>
        <button @click="showModal = false" class="bg-red-200 hover:bg-red-400 text-white cursor-pointer">Close</button>
      </div>
    </div>
    <div class="container mx-auto">
      <header>
        <h1>Notes</h1>
        <button @click="showModal = true"
          class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">+</button>
      </header>
      <div class="cards-container flex flex-wrap">
        <div class="card">
          <p class="main-text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Natus aut cumque quisquam, eaque
            eligendi omnis.</p>
          <p class="date">30/08/2023</p>
        </div>
        <div class="card">
          <p class="main-text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Natus aut cumque quisquam, eaque
            eligendi omnis.</p>
          <p class="date">30/08/2023</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  height: 100vw;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-weight: bold;
  margin-bottom: 25px;
  font-size: 75px;
}

.card {
  width: 225px;
  height: 225px;
  background-color: rgb(237, 182, 44);
  padding: 10px;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 0 20px 20px 0;
}

.date {
  font-size: 12.5px;
  font-weight: bold;
}

.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgb(0, 0, 0, 0.77);
  justify-content: center;
}
</style>