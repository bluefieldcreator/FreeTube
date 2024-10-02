<script>
  let youtube = "";
  let isActive = false;
  let output = "";
  const extractVideoURI = (link) => {output = `https://www.youtube-nocookie.com/embed/${link.split('/watch?v=')[1]}`}; 
</script>
<div>
    <div class="text-4xl font-bold m-2 text-center text-blue-600">YouTube, FreeTube</div>
    <div class="font-bold m-2 text-center text-blue-600">Un funcional desbloqueador de YouTube con fines educativos.</div>

    <div class="flex mx-12 text-center md:mx-auto md:w-2/4">
      <input class="w-3/4 border-2 focus:outline-none p-1" type="text" placeholder="URL" bind:value="{youtube}" />
      <div class="text-white font-bold bg-blue-500 p-2 hover:bg-blue-600 cursor-pointer selection:select-none" on:click={extractVideoURI(youtube)}>Desbloquear</div>
    </div>
    <div class="font-bold m-2 text-center mx-auto w-2/4 text-blue-600">Este sitio web no se hace cargo de ningun uso inadecuado de la utilidad. Los fines con los que esta creada son ultimamente educativos.</div>

    <iframe class="mx-auto p-1 border" height="500" width="1080" title="desbloqueado" src="{output}"></iframe>
</div>
