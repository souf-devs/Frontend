<template>
  <div class="container relative mx-auto pt-4 flex flex-row justify-items-center justify-between border-b border-gray-500">

    <!--LOGO-->
    <div class="w-28 h-14 mx-4">
      <img src="../assets/logo.png">
    </div>
    <!---->

    <!---->
    <!---->

  <div>
      <nav class="hidden sm:flex sm:flex-row justify-between">
        <div>
        <router-link :to="{name:'login'}" class=" px-4 text-red-500 dark:text-teal-300 text-lg  ">Login</router-link>
        </div>
        <div>
        <router-link :to="{name:'signup'}" class=" px-4 text-red-500 dark:text-teal-300 text-lg  ">Signup</router-link>
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

  
    
      <div @click="switchTheme" class="px-4">
        <svg id="sun" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="dark:text-teal-300 h-8 w-6 hidden">
        <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v2.25m6.364.386l-1.591 1.591M21 12h-2.25m-.386 6.364l-1.591-1.591M12 18.75V21m-4.773-4.227l-1.591 1.591M5.25 12H3m4.227-4.773L5.636 5.636M15.75 12a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0z" />
        </svg>
        <svg id="moon" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="text-red-500 w-6 h-8 ">
          <path stroke-linecap="round" stroke-linejoin="round" d="M21.752 15.002A9.718 9.718 0 0118 15.75c-5.385 0-9.75-4.365-9.75-9.75       0-1.33.266-2.597.748-3.752A9.753 9.753 0 003 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 009.002-5.998z" />
        </svg>
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
    switchTheme() {
      document.querySelector("#sun").classList.toggle("hidden")
      document.querySelector("#moon").classList.toggle("hidden")
      document.documentElement.classList.toggle("dark") //0658063918
      document.body.classList.toggle("bg-slate-900")
    }

  }
}
  
</script>