<template>
  <div class="container mx-auto mt-10 px-5 py-10">
    <form action="" class="flex items-center gap-3" @submit.prevent="addTask">
      <div class="p-5">
        <input
          type="text"
          placeholder="I need it"
          class="px-4 py-2 shadow-sm border border-gray-300 rounded-md placeholder-gray-400"
          v-model="taskName" />
      </div>
      <button
        type="submit"
        class="bg-blue-400 text-white px-4 py-2 rounded-md shadow-sm hover:bg-blue-500 transition-all">
        Add item
      </button>
    </form>

    <div class="justify-between flex">
      <div class="px-4 font-semibold text-gray-600">
        <p>You Have 2 Tasks to Complete</p>
      </div>
      <div class="mx-4 space-x-3">
        <button class="bg-green-200 px-5 py-1">All</button>
        <button class="bg-red-400 px-5 py-1">Favourite</button>
      </div>
    </div>

    <div
      class="flex justify-between items-center shadow-sm shadow-gray-400 px-3 py-3 mx-4 my-4"
      v-for="task in tasks">
      <div>
        <p>{{ task.title }}</p>
      </div>
      <div class="flex gap-3">
        <img src="./../assets/icons/trash-solid.svg" alt="" width="15" />
        <img src="./../assets/icons/heart.svg" alt="" width="20" />
      </div>
    </div>
    <button type="submit" class="bg-orange-500 font-semibold rounded-md px-4 py-2 mx-4">
      Reset Tasks
    </button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const tasks = ref([
  { title: "Eating", id: 1, isFavourite: false },
  { title: "Running", id: 2, isFavourite: false },
  { title: "Skipping", id: 3, isFavourite: false },
]);

const taskName = ref("");

const addTask = () => {
  const data = {
    title: taskName.value,
    id: Math.floor(Math.random() * 100) + 1,
    isFavourite: false,
  };

  tasks.value.push(data);

  console.log(tasks.value);
};
</script>
