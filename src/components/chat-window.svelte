<!-- <script>



</script>

<div class="bg-black w-full h-full text-white p-6 rounded-xl shadow-lg max-w-3xl">



</div> -->

<script lang="ts">
  import {
    AlignCenter,
    CopyIcon,
    Plus,
    ThumbsDown,
    ThumbsUp,
  } from "lucide-svelte";
  export let messages = [
    {
      id: "2",
      role: "ai",
      title:
        "ISO Certified Companies Cutting Tools Materials Made of Steel Near Me",
      content:
        "10 companies were found with ISO certification for cutting tools materials made of steel in Texas10 companies were found with ISO certification for cutting tools materials made of steel in Texas. The closest to the location you specified is company A and the furthest is company B. Companies C, D and E also manufacture equipment out of fiberglass.",
    },
    {
      id: "1",
      role: "user",
      content:
        "ISO Certified Companies Cutting Tools Materials Made of Steel Near Me",
    },
    {
      id: "2",
      role: "ai",
      title:
        "ISO Certified Companies Cutting Tools Materials Made of Steel Near Me",
      content:
        "10 companies were found with ISO certification for cutting tools materials made of steel in Texas10 companies were found with ISO certification for cutting tools materials made of steel in Texas. The closest to the location you specified is company A and the furthest is company B. Companies C, D and E also manufacture equipment out of fiberglass.",
    },
    {
      id: "1",
      role: "user",
      content:
        "ISO Certified Companies Cutting Tools Materials Made of Steel Near Me",
    },
    {
      id: "2",
      role: "ai",
      title:
        "ISO Certified Companies Cutting Tools Materials Made of Steel Near Me",
      content:
        "10 companies were found with ISO certification for cutting tools materials made of steel in Texas10 companies were found with ISO certification for cutting tools materials made of steel in Texas. The closest to the location you specified is company A and the furthest is company B. Companies C, D and E also manufacture equipment out of fiberglass.",
    },
    {
      id: "1",
      role: "user",
      content:
        "ISO Certified Companies Cutting Tools Materials Made of Steel Near Me",
    },
  ];
</script>

<!-- Outer scroll wrapper: full-width, scrollable -->
<div class="flex flex-col h-full w-full overflow-hidden">
  <!-- Scrollable content at full width -->
  <div
    class="flex-1 h-full overflow-y-auto hide-scrollbar"
  >
    <!-- Inner centered chat content -->
    <div class="max-w-4xl w-full mx-auto px-4 space-y-8 py-4">
      {#each messages as msg}
        {#if msg.role === "ai"}
          <div class="bg-black/50 p-6 rounded-2xl text-white shadow-lg">
            <h2 class="text-[20px] font-semibold leading-tight">
              {msg.title ?? "AI Response"}
            </h2>
            <p class="mt-3 text-sm leading-relaxed text-gray-300">
              {msg.content}
            </p>

            <div class="flex-col items-center gap-4 text-white">
              <div class="flex gap-4 my-4">
                <CopyIcon class="w-4 h-4 cursor-pointer hover:text-white" />
                <ThumbsUp class="w-4 h-4 cursor-pointer hover:text-white" />
                <ThumbsDown class="w-4 h-4 cursor-pointer hover:text-white" />
              </div>
              <span
                class="text-sm cursor-pointer bg-white/10 px-4 py-2 rounded-full"
              >
                Sources
              </span>
            </div>
          </div>
        {:else}
          <div class="flex justify-end">
            <div
              class="bg-blue-600 text-white rounded-xl px-5 py-3 max-w-md text-sm shadow-sm"
            >
              {msg.content}
            </div>
          </div>
        {/if}
      {/each}
    </div>
  </div>

  <!-- Input area (still centered) -->
  <div class="w-full px-4 mt-3">
    <div
      class="max-w-4xl mx-auto w-full flex flex-col bg-black/50 rounded-2xl gap-4 shadow-lg px-4 py-3"
    >
      <input
        type="text"
        placeholder="Ask me anything"
        class="w-full bg-transparent text-white/80 pb-2 outline-none placeholder:text-white/40"
      />

      <div class="flex items-center justify-between gap-4 w-full">
        <div class="flex items-center gap-4">
          <Plus class="w-6 h-6 cursor-pointer hover:text-white" />
          <span
            class="text-sm cursor-pointer bg-white/10 px-4 py-2 rounded-full"
          >
            Deep Thinking
          </span>
          <span
            class="text-sm cursor-pointer bg-white/10 px-4 py-2 rounded-full"
          >
            Search the Web
          </span>
        </div>

        <div
          class="h-12 w-12 rounded-full bg-blue-600 flex items-center justify-center cursor-pointer hover:bg-blue-700"
        >
          <img
            src="Logo.svg"
            alt="Send"
            class="w-full h-full object-contain"
          />
        </div>
      </div>
    </div>
  </div>

  <!-- Bottom spacer -->
  <div class="h-4"></div>
</div>
