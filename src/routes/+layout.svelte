<script>
  import 'virtual:windi.css'
  import { tweened } from 'svelte/motion'
  import { fly } from 'svelte/transition'
  import { interpolateLab } from 'd3-interpolate'
  import logo from '$lib/img/logo1.png'

  const bgColor = tweened('#ffffff00', {
    interpolate: interpolateLab,
    duration: 100
  })

  const textColor = tweened('#ffffffff', {
    interpolate: interpolateLab,
    duration: 100
  })

  let y = 0, w = 0
  $: if(y == 0){
    bgColor.set('#ffffff00')
    textColor.set('#ffffffff')
  } else {
    bgColor.set('#ffffffff')
    textColor.set('#000000')
  }

  let open = false

</script>

<svelte:head>
  <title>NTURPG</title> 
</svelte:head>

<svelte:window bind:scrollY={y} bind:innerWidth={w} />

<div class="fixed w-full flex px-64 <xl:px-32 <lg:px-4 py-2 shadow-lg" style:background-color={$bgColor}>

  <div class="flex items-center gap-8 flex-1">
    <img class="h-16" src={logo} alt="" />
    <span class="text-2xl" style:color={$textColor}>NTU RPG</span>
  </div>
  
  <div class="flex items-center gap-8">
    {#if w > 639}
    <a class="" href="#1">
      <span class="text-xl underline-offset-6 hover:underline" style:color={$textColor}>
        主頁
      </span>
    </a>
    <a class="" href="#2">
      <span class="text-xl underline-offset-6 hover:underline" style:color={$textColor}>
        關於
      </span>
    </a>
    <a class="" href="#3">
      <span class="text-xl underline-offset-6 hover:underline" style:color={$textColor}>
        介紹
      </span>
    </a>
    <a class="" href="#cmd">
      <span class="text-xl underline-offset-6 hover:underline" style:color={$textColor}>
        常用指令
      </span>
    </a>
    <span style:color={$textColor}>|</span>
    <a class="" href="#4">
      <span class="text-xl underline-offset-6 hover:underline" style:color={$textColor}>
        Discord
      </span>
    </a>
    {:else}
    <button on:click={()=>{open = true}}>
      <span class="text-2xl" style:color={$textColor}>
        ☰
      </span>
    </button>
    {/if}
  </div>
  
</div>

{#if open}
<div class="fixed w-full bg-white flex flex-col items-end gap-4 py-6 px-5" transition:fly={{ y: -50 }}>
  <button on:click={()=>{open = false}} class="w-max">
    <span class="text-2xl">
      X
    </span>
  </button>
  <a class="" href="#1">
    <span class="text-xl underline-offset-6 hover:underline">
      主頁
    </span>
  </a>
  <a class="" href="#2">
    <span class="text-xl underline-offset-6 hover:underline">
      關於
    </span>
  </a>
  <a class="" href="#3">
    <span class="text-xl underline-offset-6 hover:underline">
      介紹
    </span>
  </a>
  <a class="" href="#cmd">
    <span class="text-xl underline-offset-6 hover:underline">
      常用指令
    </span>
  </a>
  <span>—</span>
  <a class="" href="#4">
    <span class="text-xl underline-offset-6 hover:underline">
      Discord
    </span>
  </a>
</div>
{/if}

<slot/>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }
</style>