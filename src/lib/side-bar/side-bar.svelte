
        <script>
            export let sideBarButtonClicked  = () => {};
        </script>
        <div class="flex justify-between">
            <span class="font-bold text-2xl sm:text-3xl p-2">Sidebar</span>
            <button 
                class="p-2 rounded focus:outline-none focus:bg-indigo-800 hover:bg-indigo-800 lg:hidden"
                on:click={() => {sideBarButtonClicked()}}
            >
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M15 19l-7-7 7-7" />
                  </svg>
            </button>
        </div>
        <div>
            <ul class="mt-8">
                <li><a href="work" class="block px-4 py-2 hover:bg-indigo-800 rounded-md">Work</a></li>
                <li><a href="/about" class="block px-4 py-2 hover:bg-indigo-800 rounded-md">About</a></li>
                <li><a href="contact" class="block px-4 py-2 hover:bg-indigo-800 rounded-md">Contact</a></li>
            </ul>
        </div>
      
