<script>
  import { CircleDotDashed, Dot, DropletsIcon, Ellipsis, Menu, MenuIcon, Search } from "lucide-svelte";
  import NewChat from "./new-chat.svelte";

  let chats = [
    "ISO Certified Companies",
    "ISO Certified Companies",
    "ISO Certified Companies",
    "ISO Certified Companies",
  ];
</script>

<div class="space-y-4 h-full ">


  <NewChat />
  <div >
    <div
      class=" border-1 border-inset justify-between border-white/10 rounded-2xl backdrop-blur bg-black/30 p-2 px-3 flex items-center gap-3 hover:bg-black/20 transition-colors cursor-pointer"
    >
      <input class="text-lg px-1 text-white/50  focus:outline-none" placeholder="Search the chats"/>
      <div
        class="flex items-center text-white justify-center h-10 w-10 rounded-full cursor-pointertransition-colors"
      >
        <Search class="w-6 h-6 opacity-100" />
      </div>
    </div>
  </div>

  <!-- line break -->
  <hr class=" mx-1 border-white/10 my-4" />
  <span class="text-sm  text-white/50">Last Chats</span>
  <ul class=" space-y-2">
    
    {#each chats as chat}
    <li
    class="px-[10px] h-[49px] rounded-xl items-center justify-between flex hover:bg-black/40 cursor-pointer"
    >
        <span>
          {chat}
        </span>

        <Ellipsis class="w-6 h-6" />
      </li>
    {/each}
  </ul>
</div>
