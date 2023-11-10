<script>
  	import { onMount } from 'svelte';
 let items = ["Home","Skills","Experince","Contact"]

 let today = new Date();
 let date = today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate();
 let time = new Date();
  $: hours = time.getHours();
  $: minutes = time.getMinutes();
  $: seconds = time.getSeconds();
  $: dateTime = date+' '+hours+ ':' + minutes+ ':' + seconds;
 
  onMount(() => {
		const interval = setInterval(() => {
			time = new Date();
		}, 1000);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<header>

    <nav class="p-3 ">
        <div class="container flex flex-wrap items-center justify-between mx-auto">
          <a href="/" class="flex items-center">
              <img src="favicon.png" class="h-6  sm:h-10" alt="Logo" />
              <span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white">mmura</span>
          </a>
          <h1 class="text-black dark:text-white text-end px-6 clock">{dateTime}</h1>
          
        </div>
      </nav>
      
</header> 

<style>
.clock{
  font-family: sans-serif;
  font-style: italic;

}
</style>