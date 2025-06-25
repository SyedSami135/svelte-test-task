<script>
  import { Plus } from "lucide-svelte";
</script>

<div
  class=" border-1 border-inset border-white/10 rounded-2xl backdrop-blur bg-black/30 p-2 px-3 flex items-center gap-3 hover:bg-black/20 transition-colors cursor-pointer"
>
  <div
    class="flex items-center justify-center h-10 w-10 bg-white/20 rounded-full cursor-pointer hover:bg-white/30 transition-colors"
  >
    <Plus class="w-5 h-5 opacity-100  text-white" />
  </div>
  <span class="text-lg text-white ">New Chat</span>
</div>
