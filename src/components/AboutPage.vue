<template>
    <section class="container mx-auto py-12 px-6">
      <div class="text-center mb-20 mt-40">
        <h2 class="text-4xl font-bold text-[#434342]">About</h2>
        <div class="flex justify-center items-center">
          <hr class="w-[50px] border-[1px] mt-3 mb-3 border-teal-500">
        </div>
        <p class="text-[#434342] mt-2">Necessitatibus eius consequatur ex aliquid fuga eum quidem sint consectetur velit</p>
      </div>
  
      <div class="flex flex-col md:flex-row items-center md:items-start gap-8">
        <!-- Profile Image -->
        <div class="w-full md:w-2/4">
          <img src="/images/SamplePhoto.webp" alt="Profile" class="w-full rounded-lg shadow-lg">
        </div>
  
        <!-- Profile Details -->
        <div class="w-full md:w-2/3">
          <h3 class="text-2xl font-bold text-[#434342]">UI/UX Designer & Web Developer.</h3>
          <p class="italic mt-6 mb-8 text-[#434342]">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
  
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mt-4 text-[#434342]">
            <p><strong>📅 Birthday:</strong> 17 March 2002</p>
            <p><strong>🎂 Age:</strong> 30</p>
            <p><strong>🌐 Website:</strong> <a href="#" class="text-blue-600 hover:underline">www.example.com</a></p>
            <p><strong>🎓 Degree:</strong> Master</p>
            <p><strong>📞 Phone:</strong> +123 456 7890</p>
            <p><strong>📧 Email:</strong> <a href="mailto:email@example.com" class="text-blue-600 hover:underline">email@example.com</a></p>
            <p><strong>📍 City:</strong> New York, USA</p>
            <p><strong>💼 Freelance:</strong> Available</p>
          </div>
  
          <p class="mt-6 text-gray-600">
            Officiis eligendi itaque labore et dolorum mollitia officiis optio vero. Quisquam sunt adipisci omnis et ut. Nulla accusantium dolor incidunt officia tempore. Et eius omnis. Cupiditate ut dicta maxime officiis quidem quia. Sed et consectetur qui quia repellendus itaque neque.
          </p>
        </div>
      </div>
    </section>
    
    <section>
      <div class="text-center mb-5 mt-[100px] px-6">
        <h2 class="text-4xl font-bold text-[#434342]">Skills</h2>
          <div class="flex justify-center items-center">
            <hr class="w-[50px] border-[1px] mt-3 mb-3 border-teal-500">
          </div>
          <p class="text-[#434342] mt-2">Necessitatibus eius consequatur ex aliquid fuga eum quidem sint consectetur velit</p>
      </div>

      <div class="container mx-auto py-12 px-6 mb-20">
        <div class="grid grid-cols-2 gap-6">
          <div 
            v-for="(skill, index) in skills" 
            :key="skill.name"
            ref="skillBars"
            class="opacity-0 transform translate-y-6 transition-all duration-1000 ease-in-out delay-[index*200] "
            :class="{ 'opacity-100 translate-y-0': isVisible[index] }"
          >
        <div class="flex justify-between font-bold mb-1">
          <span>{{ skill.name }}</span>
          <span>{{ skill.level }}%</span>
        </div>
        <div class="bg-gray-200 h-2 rounded-lg relative">
          <div 
            class="bg-teal-500 h-2 rounded-lg transition-all duration-700 ease-in-out"
            :style="{ width: isVisible[index] ? skill.level + '%' : '0%' }"
          ></div>
        </div>
      </div>
    </div>
  </div>
</section>
</template>
  
  <script>
export default {
  data() {
    return {
      skills: [
        { name: "HTML", level: 100 },
        { name: "PHP", level: 80 },
        { name: "CSS", level: 90 },
        { name: "WordPress/CMS", level: 90 },
        { name: "JavaScript", level: 75 },
        { name: "Photoshop", level: 55 }
      ],
      isVisible: []
    };
  },
  mounted() {
    this.observeElements();
  },
  methods: {
    observeElements() {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        const index = this.$refs.skillBars.indexOf(entry.target);
        if (index !== -1) this.isVisible[index] = true; // Vue 3 update
      }
    });
  }, { threshold: 0.3 });

  this.$refs.skillBars.forEach((el, index) => {
    this.isVisible[index] = false; // Initialize state properly
    observer.observe(el);
  });
}
  }
};
</script>

<style scoped>
/* No additional styles needed, Tailwind handles it */
</style>