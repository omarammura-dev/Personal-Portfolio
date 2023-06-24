<script>
  import { Card } from "flowbite-svelte";
  import Rating from "./rating.svelte";
</script>

<Card padding="none" size="xl" class="grid md:grid-cols-2">
   <figure class="flex flex-col justify-center items-center p-8 text-center bg-white rounded-t-lg border-b border-gray-200 md:rounded-t-none md:rounded-tl-lg md:border-r dark:bg-gray-800 dark:border-gray-700">
       <blockquote class="mx-auto mb-4 max-w-2xl text-gray-500 dark:text-gray-400">
           <p class="my-4 font-light">"the best person with amazing skills, completed the task before the deadline, really happy from the service..."</p>
       </blockquote>
       <Rating/>
       <figcaption class="flex justify-center items-center space-x-3">
           <img class="w-9 h-9 rounded-full" src="1.webp" alt="Karen profile">
           <div class="space-y-0.5 font-medium dark:text-white text-left">
               <div>anand_garg</div>
               <div class="text-sm font-light text-gray-500 dark:text-gray-400">Fiverr Customer</div>
           </div>
       </figcaption>
   </figure>
   <figure class="flex flex-col justify-center items-center p-8 text-center bg-white rounded-tr-lg border-b border-gray-200 dark:bg-gray-800 dark:border-gray-700">
       <blockquote class="mx-auto mb-4 max-w-2xl text-gray-500 dark:text-gray-400">
           <p class="my-4 font-light">"Professional and smart person. he performed the work perseveringly and perfectly, in a problem that seemed unsolvable and went beyond expectations for sure in the future I will work with him again more than recommended if you want a competent and serious person you have chosen the right person for a job"<br/>(Translated from italian)</p>
       </blockquote>
       <Rating/>
       <figcaption class="flex justify-center items-center space-x-3">
           <img class="w-9 h-9 rounded-full" src="2.webp" alt="amebaldo47">
           <div class="space-y-0.5 font-medium dark:text-white text-left">
               <div>amebaldo47</div>
               <div class="text-sm font-light text-gray-500 dark:text-gray-400">Fiverr Customer</div>
           </div>
       </figcaption>
   </figure>
   <figure class="flex flex-col justify-center items-center p-8 text-center bg-white rounded-bl-lg border-b border-gray-200 md:border-b-0 md:border-r dark:bg-gray-800 dark:border-gray-700">
       <blockquote class="mx-auto mb-4 max-w-2xl text-gray-500 dark:text-gray-400">
           <p class="my-4 font-light">"Amazing fast and great support :)"</p>
       </blockquote>
       <Rating/>
       <figcaption class="flex justify-center items-center space-x-3">
           <img class="w-9 h-9 rounded-full" src="user.png" alt="axrinas">
           <div class="space-y-0.5 font-medium dark:text-white text-left">
               <div>axrinas</div>
               <div class="text-sm font-light text-gray-500 dark:text-gray-400">Fiverr Customer</div>
           </div>
       </figcaption>
   </figure>
   <figure class="flex flex-col justify-center items-center p-8 text-center bg-white rounded-bl-lg border-b border-gray-200 md:border-b-0 md:border-r dark:bg-gray-800 dark:border-gray-700">
    <blockquote class="mx-auto mb-4 max-w-2xl text-gray-500 dark:text-gray-400">
        <p class="my-4 font-light">"Eng. Omar is a very professional designer for websites and Apps related work. We are relaying on him for all of our requirements on such service. We hope the best for him.
            "</p>
    </blockquote>
    <Rating/>
    <figcaption class="flex justify-center items-center space-x-3">
        <img class="w-9 h-9 rounded-full" src="4.png" alt="axrinas">
        <div class="space-y-0.5 font-medium dark:text-white text-left">
            <div>Ahmed Said</div>
            <div class="text-sm font-light text-gray-500 dark:text-gray-400">MYRCLLC CEO</div>
        </div>
    </figcaption>
</figure>
</Card>
