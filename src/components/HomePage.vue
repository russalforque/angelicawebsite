<template>
    <div class="w-full h-screen flex items-center justify-center bg-cover bg-center" :style="{ backgroundImage: 'url(/images/Angelicas.jpg)' }">
        <div class="text-center">
            <h1 class="text-5xl font-bold text-[#434342]">Angelica Yap</h1>
            <h6 class="text-2xl font-semibold mt-4 mb-10 text-[#434342]">I'm a Real Estate Agent from Cebu City</h6>
            <button type="button" 
                    class="text-white bg-[#34b7a7] hover:bg-[#3cd1c0] font-medium rounded-full text-sm px-5 py-2.5 w-1/3">
                ABOUT ME
            </button>
        </div>
    </div>
</template>



<script>
export default {
    name: 'HomePage'
}
</script>