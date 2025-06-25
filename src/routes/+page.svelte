<script>
  import ChatWindow from "../components/chat-window.svelte";
  import Sidebar from "../components/sidebar.svelte";
</script>

<div class="relative h-screen w-screen text-white overflow-hidden">
  <!-- Background layer -->
  <div class="absolute inset-0 -z-10 bg-black/98 opacity-90"></div>

  <!-- Main layout wrapper using flex -->
  <div class="flex h-full ">
    <!-- Sidebar -->
    <aside class="w-80 h-full p-4 border-r border-white/10 bg-black/30 text-white shadow-lg">
      <Sidebar />
    </aside>

    <!-- Main chat area: grows automatically -->
    <main class="flex-1 flex flex-col  text-white overflow-hidden">
      <ChatWindow />
    </main>
  </div>
</div>
