<script>
  let { children } = $props();
  import "../app.css";
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";

  let y;
  let innerHeight = $state(0);
  let innerWidth = $state(0);

  function goTop() {
    document.body.scrollIntoView();
  }
</script>

<!-- svelte-ignore slot_element_deprecated -->
<div
  class="container relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen"
>
  <div
    class={"fixed bottom-0 w-full duration-200 flex p-10 z-[10] " +
      (y > 0
        ? " opacity-full pointer-events-auto"
        : " pointer-events-none opacity-0")}
  >
    <button 
      onclick={goTop}
      class="ml-auto rounded-full aspect-square bg-slate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer aspect-square grid place-items-center">
      <i class="fa-solid fa-arrow-up"></i>
    </button>
  </div>
  <Header {y} {innerHeight}/>
  <slot />
  <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
