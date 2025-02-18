<template>
  <nav class="bg-[#e9e8e6] h-[90px] border-gray-200 dark:bg-gray-900 fixed top-0 w-full z-50 shadow-[-1px_8px_100px_-3px_rgba(0,_0,_0,_0.1)]">
    <div class="flex flex-wrap items-center justify-between mx-auto p-4">
      <a class="flex items-center space-x-3 rtl:space-x-reverse mt-3">
        <span class="self-center font-light text-3xl whitespace-nowrap text-[#434342] tracking-normal">ANGEL</span>
      </a>
      <div class="flex md:order-2 space-x-3 md:space-x-0 rtl:space-x-reverse mt-2">
        <div class="social-icons hidden md:flex gap-2 mr-5">
          <i class="fa-brands fa-x-twitter text-lg text-[#a1a19f] md:hover:text-[#34b7a7]"></i>
          <i class="fa-brands fa-facebook text-lg text-[#a1a19f] md:hover:text-[#34b7a7]"></i>
          <i class="fa-brands fa-instagram text-lg text-[#a1a19f] md:hover:text-[#34b7a7]"></i>
          <i class="fa-brands fa-linkedin text-lg text-[#a1a19f] md:hover:text-[#34b7a7]"></i>
        </div>
        <button data-collapse-toggle="navbar-cta" type="button"
          class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
          aria-controls="navbar-cta" aria-expanded="false">
          <span class="sr-only">Open main menu</span>
          <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M1 1h15M1 7h15M1 13h15" />
          </svg>
        </button>
      </div>
  
      <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1 mt-2" id="navbar-cta">
  <ul class="flex flex-col p-4 md:p-0 mt-4 border rounded-lg md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0">
    <li>
      <router-link to="/" class="relative block py-2 px-3 md:p-0 font-normal text-[#4b4b4b] rounded-sm hover:bg-gray-100 md:hover:bg-transparent md:hover:text-[#34b7a7] before:absolute before:bottom-0 before:left-0 before:w-1/2 before:h-[2px] before:bg-[#34b7a7] before:scale-x-0 before:origin-left before:transition-transform before:duration-300 hover:before:scale-x-100">Home</router-link>
    </li>
    <li>
      <router-link to="/about" class="relative block py-2 px-3 md:p-0 font-normal text-[#4b4b4b] rounded-sm hover:bg-gray-100 md:hover:bg-transparent md:hover:text-[#34b7a7] before:absolute before:bottom-0 before:left-0 before:w-1/2 before:h-[2px] before:bg-[#34b7a7] before:scale-x-0 before:origin-left before:transition-transform before:duration-300 hover:before:scale-x-100">About</router-link>
    </li>
    <li>
      <router-link to="/resume" class="relative block py-2 px-3 md:p-0 font-normal text-[#4b4b4b] rounded-sm hover:bg-gray-100 md:hover:bg-transparent md:hover:text-[#34b7a7] before:absolute before:bottom-0 before:left-0 before:w-1/2 before:h-[2px] before:bg-[#34b7a7] before:scale-x-0 before:origin-left before:transition-transform before:duration-300 hover:before:scale-x-100">Resume</router-link>
    </li>
    <li>
      <a href="#"
        class="relative block py-2 px-3 md:p-0 font-normal text-[#4b4b4b] rounded-sm hover:bg-gray-100 md:hover:bg-transparent md:hover:text-[#34b7a7] before:absolute before:bottom-0 before:left-0 before:w-1/2 before:h-[2px] before:bg-[#34b7a7] before:scale-x-0 before:origin-left before:transition-transform before:duration-300 hover:before:scale-x-100">
        Services</a>
    </li>
    <li>
      <router-link to="/" class="relative block py-2 px-3 md:p-0 font-normal text-[#4b4b4b] rounded-sm hover:bg-gray-100 md:hover:bg-transparent md:hover:text-[#34b7a7] before:absolute before:bottom-0 before:left-0 before:w-1/2 before:h-[2px] before:bg-[#34b7a7] before:scale-x-0 before:origin-left before:transition-transform before:duration-300 hover:before:scale-x-100">Portfolio</router-link>
    </li>
    <li>
      <a href="#"
        class="relative block py-2 px-3 md:p-0 font-normal text-[#4b4b4b] rounded-sm hover:bg-gray-100 md:hover:bg-transparent md:hover:text-[#34b7a7] before:absolute before:bottom-0 before:left-0 before:w-1/2 before:h-[2px] before:bg-[#34b7a7] before:scale-x-0 before:origin-left before:transition-transform before:duration-300 hover:before:scale-x-100">
        Contact</a>
    </li>
  </ul>
</div>

    </div>
  </nav>
  <router-view/>
  </template>
  

<script>
export default {
    name: 'NavBar'
}
</script>

<style scoped>

</style>