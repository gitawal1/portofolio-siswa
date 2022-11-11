<script setup>
import { ref } from "vue";

const nama = ref("");
const kelas = ref("");
const tanggal = ref("");
const image = ref("");
const desc = ref("");
</script>
<template>
  <div class="container px-2 mt-4">
    <div class="md:w-1/2 mx-auto justify-center p-5 bg-slate-100">
      <form action="">
        <div class="form-group">
          <label for="nama">Nama</label>
          <input
            type="text"
            v-model="nama"
            class="p-2 border border-spacing-1 w-full"
          />
        </div>
        <div class="form-group">
          <label for="kelas">Kelas</label>
          <input
            type="text"
            v-model="kelas"
            class="p-2 border border-spacing-1 w-full"
          />
        </div>
        <div class="form-group">
          <label for="tanggal">Tanggal</label>
          <input type="date" v-model="tanggal" />
        </div>
        <div class="form-group">
          <label for="image">Image</label>
          <input type="file" @change="setImage" />
        </div>
        <div class="form-group">
          <label for="desc">Deskripsi</label>
          <textarea name="" id="" cols="30" rows="10" v-model="desc"></textarea>
        </div>
        <button
          class="bg-cyan-400 text-white py-2 px-4 rounded-sm duration-500 hover:bg-cyan-500 mx-4 md:my-0"
        >
          Submit
        </button>
      </form>
    </div>
  </div>
</template>
