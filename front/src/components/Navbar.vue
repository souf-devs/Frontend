<template>
  <div class="container relative mx-auto pt-4 flex flex-row justify-between border-b border-gray-500">
    <div class="w-28 h-14 mx-4">
      <img src="../assets/logo.png">
    </div>
  <nav class="hidden sm:flex sm:flex-row justify-between">

    <div>
    <router-link :to="{name:'login'}" class=" px-4 text-red-500 text-lg  ">Login</router-link>
    </div>
    <div>
    <router-link :to="{name:'signup'}" class=" px-4 text-red-500 text-lg  ">Signup</router-link>
    </div>
  </nav>
  
<svg @click="showMenu" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="sm:hidden w-8 h-8 text-red-500 hover:text-gray-900 mr-4 cursor-pointer ">
  <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
</svg>

  <div id="menu" class="hidden right-0 mt-6 mr-12  flex flex-col shadow-black shadow-md justify-between bg-white">

    <div>
    <router-link :to="{name:'login'}"><div class ="py-2  px-14 text-red-500 border-b border-gray-500 hover:text-gray-600 hover:shadow-xl">Login</div></router-link>
    </div>
    <div>
    <router-link :to="{name:'signup'}"><div class ="py-2  px-14 text-red-500 border-b border-gray-500 hover:text-gray-600 hover:shadow-xl"> Signup</div></router-link>
    </div>
  </div>
</div>
  
</template>


<script>

export default {
  methods: {

    showMenu() {
      const menu = document.querySelector("#menu")
      if(menu.classList.contains("hidden")) {
          menu.classList.remove("hidden");
          menu.classList.add("absolute");
        }else {
          menu.classList.add("hidden");
          menu.classList.remove("absolute");

        }
    },
  }
}
  
</script>