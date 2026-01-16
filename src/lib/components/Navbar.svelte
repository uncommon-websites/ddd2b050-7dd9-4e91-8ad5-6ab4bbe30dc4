<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 50;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<div class="fixed w-full z-50 transition-colors duration-300 top-0 left-0 text-gray-900 font-sans">
  <!-- Top Bar -->
  <div class="bg-primary-100 text-[11px] font-medium tracking-wide text-center py-2.5 flex justify-center items-center gap-1 cursor-pointer hover:underline text-primary-900">
    <span>Book your stress-free studio fitting in Singapore today</span>
    <span class="text-[10px]">➜</span>
  </div>

  <!-- Main Nav -->
  <nav class="flex justify-between items-center px-6 py-4 md:px-10 transition-all duration-300 {isScrolled ? 'bg-white/90 backdrop-blur-md shadow-sm py-3 text-gray-900' : 'bg-transparent text-white'}">
    <!-- Left Links -->
    <div class="hidden md:flex items-center gap-8 text-[13px] font-medium tracking-wide">
      <a href="/" class="hover:opacity-60 transition-opacity">Gowns</a>
      <a href="/" class="hover:opacity-60 transition-opacity">Our Studio</a>
      <a href="/" class="hover:opacity-60 transition-opacity">Pricing</a>
    </div>

    <!-- Logo -->
    <div class="absolute left-1/2 transform -translate-x-1/2">
      <a href="/" class="block flex items-center">
        <svg width="40" height="44" viewBox="0 0 87 96" fill="none" xmlns="http://www.w3.org/2000/svg" class="{isScrolled ? 'text-gray-900' : 'text-white'}">
          <path fill-rule="evenodd" clip-rule="evenodd" d="M59.9489 37.1809C58.7302 49.9289 48.0665 59.8958 35.092 59.8958C32.3768 59.8958 29.763 59.4593 27.3158 58.6524C28.5345 45.9044 39.198 35.9375 52.1725 35.9375C54.8877 35.9375 57.5015 36.374 59.9489 37.1809ZM58.8631 27.0075C56.6988 26.5789 54.4617 26.3542 52.1725 26.3542C35.7001 26.3542 21.9251 37.9879 18.5029 53.5438C13.3593 48.9359 10.119 42.2189 10.119 34.7396C10.119 20.8461 21.2998 9.58333 35.092 9.58333C46.2061 9.58333 55.6247 16.8971 58.8631 27.0075ZM69.3789 30.9803C67.5183 13.5622 52.8775 0 35.092 0C16.0456 0 0.605469 15.5535 0.605469 34.7396C0.605469 47.6136 7.55728 58.852 17.8857 64.8531C19.7463 82.2712 34.3872 95.8333 52.1725 95.8333C71.219 95.8333 86.659 80.2798 86.659 61.0938C86.659 48.2197 79.7072 36.9816 69.3789 30.9803ZM68.7617 42.2896C65.3395 57.8455 51.5644 69.4792 35.092 69.4792C32.8028 69.4792 30.5659 69.2544 28.4016 68.8258C31.64 78.9362 41.0584 86.25 52.1725 86.25C65.9647 86.25 77.1455 74.9872 77.1455 61.0938C77.1455 53.6144 73.9054 46.8975 68.7617 42.2896Z" fill="currentColor"/>
        </svg>
      </a>
    </div>

    <!-- Right Links -->
    <div class="flex items-center gap-6 md:gap-8">
      <a href="/" class="text-[13px] font-medium tracking-wide hover:opacity-60 transition-opacity hidden md:block">Location</a>
      <a href="/" class="{isScrolled ? 'bg-primary-600 text-white' : 'bg-white text-gray-900'} px-5 py-2 rounded-full text-[13px] font-bold tracking-wide hover:opacity-90 transition-all shadow-sm">Book Fitting</a>
      <button class="md:hidden">
        <!-- Mobile Menu Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </button>
    </div>
  </nav>
</div>

<style>
    /* Adjust logo to match brand aesthetic */
</style>
