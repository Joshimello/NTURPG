<script>
  import img1 from '$lib/img/1.png'
  import img2 from '$lib/img/2.png'
  import logo2 from '$lib/img/logo2.png'
  import img3 from '$lib/img/3.png'
  import img4 from '$lib/img/4.png'
  import img5 from '$lib/img/5.png'
  import img6 from '$lib/img/6.png'

  const cmds = [
    ['/spawn', '- 回到主城。'],
  	['/skill', '- 查看自己的技能列表。'],
  	['/skill lang zh-CN', '- 設置中文語言。'],
  	['/msg ID', '- 私訊玩家。'],
  	['/hat', '- 把手上拿著的東西帶上頭。'],
  	['/sethome <英文名稱>', '- 設置家的位置傳送。'],
  	['/delhome <英文名稱>', '- 刪除家的位置傳送。'],
  	['/home <英文名稱>', '- 傳送到設置家的位置。']
  ]

</script>

<div class="w-full h-100vh" id="1">
  <img class="w-full h-full object-cover absolute -z-1" src={img1} alt=""/>
  <div class="w-full h-full flex flex-col px-64 py-50 <xl:px-32 <sm:px-8">
    <div class="flex flex-col gap-4 flex-1">
      <span class="text-white text-4xl">
        NTU RPG
      </span>
      <span class="text-white text-lg">
        一個休閑的好地方~
      </span>
    </div>
    <div class="flex items-end justify-end">
      <a class="text-white border-2 px-8 py-4 rounded-full <sm:w-full" href="#2">
        <span class="text-white text-2xl">
          了解更多
        </span>
      </a>
    </div>
  </div>
</div>

<div class="w-full flex gap-8 px-64 <xl:px-32 <lg:px-4 py-16 <sm:flex-col" id="2">
  <div class="flex-1">
    <img class="" src={img2} alt=""/>
  </div>
  <div class="flex-1 flex flex-col gap-4 items-center justify-center">
    <span class="text-4xl">
      關於
    </span>
    <span class="text-lg text-center">
      你從Minecraft世界打破了世界邊界，來到了異世界！<br>
      你將在異世界冒險，和跟著故事主綫一起<br>
      體驗劇情和欣賞風景！<br>
    </span>
  </div>
</div>

<div class="w-full flex flex-col items-center justify-center p-16 border-y-3" id="3">
  <img src={logo2} alt=""/>
  <span class="text-4xl pt-6">
    認識 NTURPG
  </span>
  <span class="text-lg pt-2">
    歡迎來到RPG世界！
  </span>
</div>

<div class="w-full flex flex-col items-center justify-center p-16 border-b-3">
  <span class="text-4xl pt-6">
    IP: nturpg.xyz
  </span>
  <span class="text-lg pt-2">
    版本：1.20.1
  </span>
</div>

<div class="w-full flex flex-col gap-16 px-64 <xl:px-32 <lg:px-4 py-16 <sm:flex-col">
  <div class="w-full flex items-center justify-center">
    <span class="text-4xl">
      伺服器展示
    </span>
  </div>
  <div class="grid grid-cols-2 gap-8 <sm:grid-cols-1">
    <div class="flex flex-col items-center gap-2">
      <img src={img3} alt=""/>
      <span class="text-xl">
        副本小鎮
      </span>
    </div>
    <div class="flex flex-col items-center gap-2">
      <img src={img4} alt=""/>
      <span class="text-xl">
        精靈古樹
      </span>
    </div>
    <div class="flex flex-col items-center gap-2">
      <img src={img5} alt=""/>
      <span class="text-xl">
        月宮
      </span>
    </div>
    <div class="flex flex-col items-center gap-2">
      <img src={img6} alt=""/>
      <span class="text-xl">
        大和島國
      </span>
    </div>
  </div>
</div>

<div class="w-full flex flex-col gap-4 px-64 border-y-3 items-center <xl:px-32 <lg:px-4 py-16 <sm:flex-col " id="cmd">
  <span class="text-4xl mb-16">
    伺服器常用指令
	</span>
	{#each cmds as [cmd, desc]}
    <div class="flex gap-2 items-center justify-center">
      <span class="text-xl bg-gray-200 rounded-xl py-2 px-4 font-mono">
        {cmd}
      </span>
      <span class="text-xl">
        {desc}
      </span>
    </div>
  {/each}
</div>

<div class="w-full flex flex-col gap-4 items-center justify-center p-16 border-y-3" id="4">
  <span class="text-4xl">
    加入我們 Discord!
  </span>
  <span class="text-lg">
    Discord: <a class="underline" target="_blank" href="https://discord.gg/FzmF6ZBxkb">https://discord.gg/FzmF6ZBxkb</a>
  </span>
  <iframe src="https://discord.com/widget?id=1081818193158479892&theme=dark" width="350" height="500" allowtransparency="true" frameborder="0" sandbox="allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts"></iframe>
</div>

<div class="w-full h-50vh"></div>
