<script>
    import Head from '$lib/header.svelte'
    import Footer from '$lib/footer.svelte'
    import Tab from '$lib/tab.svelte'
    import Contact from '$lib/contact.svelte'
    import Experinces from '../lib/experinces.svelte';
    import { Hr } from 'flowbite-svelte'
    
    let tabs = [{title:"Android development",p:"just text for Android"},{title:"AI",p:"just text for AI"},{title:"Competetive Programming",p:"just text for cp"},{title:"DevOps",p:"just text for Devops"}];
    let experinces= [{title:"dummy",date:"dummy ",p:"jgjdummygj"},{title:"dummy",date:"dummy",p:"dummy"},{title:"dummy",date:"dummy",p:"dummy"}]
    let  currentTab = 'Web development';
</script>


<div class="container px-10">
<Head />
    <section class="p-3">
        <img class="rounded-full w-60 h-60 mx-auto" src="/1.png" alt="MyImage">
        <h1 class="mb-4 text-3xl text-center font-extrabold  text-gray-900 dark:text-white md:text-5xl lg:text-6xl"><span class="text-transparent bg-clip-text bg-gradient-to-r to-emerald-600 from-sky-400">Omar Ammura</span></h1>
        <p class="text-lg font-normal text-gray-500 lg:text-xl  dark:text-gray-400 text-center">Computer Engineering Student</p>
        <p class="text-lg font-normal text-gray-500 lg:text-xl  dark:text-gray-400 text-center py-6">Creative Web and Mobile App Developer with a talent for problem-solving</p>
    </section>
<div id="Skills">
    <h1 class="text-7xl py-5 font-extrabold dark:text-white text-center mt-20 font-serif">Skills</h1>
    <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 dark:bg-gray-700">

</div>
    <section>
        <Tab {tabs}/> 
    </section>

    <div id="Experince">
        <h1 class="text-7xl py-5 font-extrabold dark:text-white text-center mt-20 font-serif">Experinces</h1>
        <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 dark:bg-gray-700">
    
    </div>    
    <Experinces {experinces}/>
    <div id="Contact">
        <h1 class="text-7xl py-5 font-extrabold dark:text-white text-center mt-20 font-serif">Contact Us</h1>
        <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 dark:bg-gray-700">
    
    </div>  
    <section>
       <Contact/>
    </section>
    <Hr class="my-5" height="h-px" />

<Footer/>    
</div>    

<style>
   
</style>


