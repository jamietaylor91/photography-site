<script>
    import "../app.css";
    import Sidebar from '../lib/side-bar/side-bar.svelte';

    let isOpen = false;
    const sideBarButtonClicked = () => {
      isOpen = !isOpen;
    }
</script>
<div class="min-h-screen lg:flex">
  <nav 
    class="absolute inset-0 transform duration-200 lg:transform-none lg:opacity-100 lg:relative z-10 w-80 bg-indigo-900 text-white h-screen p-3" 
    class:translate-x-0="{isOpen}"
    class:ease-in="{isOpen}"


    class:-translate-x-full="{isOpen === false}"
    class:ease-out="{isOpen === false}"
    class:opacity-0="{isOpen == false}"

  >
    <Sidebar sideBarButtonClicked={sideBarButtonClicked} />
  </nav>
  <div class="relative z-0 lg:flex-grow">
    <header class="flex bg-gray-700 text-white items-center px-3">
      <button class="p-2 rounded-md focus:outline-none focus:bg-gray-600 hover:bg-gray-600 lg:hidden"
      on:click={() => {sideBarButtonClicked()}}
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
      <span class="text-2xl sm:text-3xl font-bold text-white p-4">Jamie's Photography</span>
    </header> 
  </div>
  <slot />
</div>

