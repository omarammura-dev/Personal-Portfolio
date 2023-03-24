<script>
    import Head from '$lib/header.svelte'
    import Footer from '$lib/footer.svelte'
    import Tab from '$lib/tab.svelte'
</script>

<Head />
<div class="container  py-6 px-5 ">
    <section class="p-3 ">
        <img class="rounded-full w-60 h-60 mx-auto" src="/1.png" alt="MyImage">
        <h1 class="mb-4 text-3xl text-center font-extrabold  text-gray-900 dark:text-white md:text-5xl lg:text-6xl"><span class="text-transparent bg-clip-text bg-gradient-to-r to-emerald-600 from-sky-400">Omar Ammura</span></h1>
        <p class="text-lg font-normal text-gray-500 lg:text-xl  dark:text-gray-400 text-center">Computer Engineering Student</p>
        <p class="text-lg font-normal text-gray-500 lg:text-xl  dark:text-gray-400 text-center py-6">Creative Web and Mobile App Developer with a talent for problem-solving</p>
    </section>
    <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 dark:bg-gray-700">
    <section>
       <div class="flex flex-wrap text-sm font-medium text-center text-gray-500 border-b border-gray-200 dark:border-gray-700 dark:text-gray-400 justify-center">
        <Tab name="Web development"/> 
        <Tab name="Android development"/>
        <Tab name="AI"/>
        <Tab name="Competetive Programming"/>
        <Tab name="RPA"/>
       </div>
    </section>
<Footer/>


</div>