<script>
  export let y;
  let showModal = false;

  let tabs = [
    { name: "Projects", link: "#projects" },
    { name: "About me", link: "#about" },
  ];

  const toggleModal = () => {
    showModal = !showModal;
  };
</script>

<header
  class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid" +
    (y > 0
      ? " py-4 bg-slate-950 border-violet-950"
      : " py-6 bg-transparent border-transparent ")}
>
  <h1 class="font-medium">
    <b class="font-bold poppins">Andres</b> Garcia
  </h1>
  <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
    {#each tabs as tab, index}
      <a href={tab.link} class="duration-200 hover:text-violet-400">
        <p>{tab.name}</p>
      </a>
    {/each}
  </div>
  <button
    on:click={toggleModal}
    class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
  >
    <div
      class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
    ></div>
    <h4 class="relative z-9">Get in touch</h4>
  </button>
</header>

{#if showModal}
  <div
    class="fixed inset-0 flex items-center justify-center bg-black/60 z-50"
    on:click={toggleModal}
  >
    <div
      class="bg-white text-black p-6 rounded-lg shadow-xl relative w-80 max-w-full"
      on:click|stopPropagation
    >
      <button
        class="absolute top-2 right-2 text-gray-500 hover:text-black text-lg"
        on:click={toggleModal}
        aria-label="Close"
      >
        ×
      </button>
      <h2 class="text-xl font-semibold mb-4">Contact Me</h2>
      <p>
        <strong>Email:</strong>
        <a
          href="mailto:andresgarcia282@gmail.com"
          class="text-violet-600 underline hover:text-violet-800"
        >
          andresgarcia282@gmail.com
        </a>
      </p>
      <p class="mt-2">
        <strong>Phone:</strong>
        <a
          href="tel:+15879369900"
          class="text-violet-600 underline hover:text-violet-800"
        >
          +1 (587) 936-9900
        </a>
      </p>
    </div>
  </div>
{/if}
