<script>
    import "../app.css";
    import Sidebar from '../lib/side-bar/side-bar.svelte';
</script>
<div class="min-h-screen lg:flex">
  <nav class="absolute inset-0 transform -translate-x-full lg:relative z-10 w-80 bg-indigo-900 text-white h-screen p-3">
    <Sidebar />
  </nav>
  <div class="relative z-0 lg:flex-grow">
    <header class="flex bg-gray-700">
      <button class="p-2 rounded focus:outline-none focus:bg-gray-600 hover:bg-gray-600">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
      <span class="text-2xl sm:text-3xl font-bold text-white p-4">Jamie's Photography</span>
    </header> 
  </div>
  <slot />
</div>

