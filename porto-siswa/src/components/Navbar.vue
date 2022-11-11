<template>
  <nav
    class="bg-slate-100 p-5 shadow md:flex md:items-center md:justify-between"
  >
    <div class="flex items-center justify-between bg-slate-100">
      <span>
        <img
          class="h-10 inline cursor-pointer"
          src="data:image/png;base64,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"
          alt=""
        />
        <span class="text-2xl font-sans font-semibold"> Sman9Lutra </span>
      </span>
      <span class="text-3xl block md:hidden mx-2 cursor-pointer">
        <ion-icon :name="iconName" @click="Menu"></ion-icon>
      </span>
    </div>
    <div>
      <ul
        class="md:flex md:items-center md:z-auto md:static absolute bg-slate-100 left-0 w-full md:w-auto md:py-0 py-4 md:pl-0 pl-7 md:opacity-100 opacity-0 top-min[-400px] transition-all ease-in duration-500"
      >
        <li class="my-6 md:my-0 mx-4">
          <a
            class="text-xl hover:text-cyan-500 duration-500 cursor-pointer"
            href="#"
            >Home</a
          >
        </li>
        <li class="my-6 md:my-0 mx-4">
          <a
            class="text-xl hover:text-cyan-500 duration-500 cursor-pointer"
            href="#"
            >About</a
          >
        </li>
        <li class="my-6 md:my-0 mx-4">
          <a
            class="text-xl hover:text-cyan-500 duration-500 cursor-pointer"
            href="#"
            >Contact</a
          >
        </li>
        <li class="my-6 md:my-0 mx-4">
          <a
            class="text-xl hover:text-cyan-500 duration-500 cursor-pointer"
            href="#"
            >Service</a
          >
        </li>
        <button
          class="bg-cyan-400 text-white py-2 px-4 rounded-sm duration-500 hover:bg-cyan-500 mx-4 md:my-0"
        >
          Get Started
        </button>
      </ul>
    </div>
  </nav>
  <div id="ruang"></div>
</template>
<script setup>
import { ref } from "vue";

const iconName = ref("menu");
let nav = document.querySelector("#ruang");

const Menu = () => {
  let list = document.querySelector("ul");
  if (iconName.value === "menu") {
    iconName.value = "close";
    list.classList.add("top-[80px]");
    list.classList.add("opacity-100");
    nav.classList.add("mb-80");
  } else {
    iconName.value = "menu";
    list.classList.remove("top-[80px]");
    list.classList.remove("opacity-100");
    nav.classList.remove("mb-80");
  }
};
</script>
<style scoped></style>
