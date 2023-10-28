<script>
    import { Tabs, TabItem } from 'flowbite-svelte';
    import { Badge } from 'flowbite-svelte';
</script>

<Tabs class="justify-center bg-slate-800">
    <TabItem  open title="Web development" color="green" class="bg-slate-800">
      <div class="grid gap-4 grid-cols-4 grid-rows-1 grid-cols-responsive bg-slate-800">
        <div class="">
            <h1 class="text-white font-bold">#2019</h1>
            <p class="text-sm text-gray-500 dark:text-gray-400">The journey of learning programming has begun. I started learning html and css based on tips I gathered from the internet. I designed simple websites, login forms, etc. - it was a really fun experience - after that I wanted to develop myself and move to a higher level in creating websites ... I wanted to add life to the site through Javascript.</p>
        </div>
        <div>
            <h1 class="text-white font-bold">#2020</h1>
            <p class="text-sm text-gray-500 dark:text-gray-400">Here I began to wonder about how to register the user on the site and show information pertaining only to the user himself, and after a little research, I realized that PHP is what I want ... I started to learn and delve into it from there. I created a simple web application through which a new user can be registered, logged in and displays a page Simple for the user himself, only of course I dealt with the MySql database.</p>
        </div>
        <div> 
            <h1 class="text-white font-bold">#2022</h1>
            <p class="text-sm text-gray-500 dark:text-gray-400">Here I started getting acquainted with JavaScript frameworks, and I liked the idea of a one-page application very much (it bothered me to reload the site every time I moved). I read about React in one of the famous blogs, after which I liked the way it works... I started to learn it (superficially). I didn't want to go deeper because I was busy with the university exam. After the exam I came back to learn full stack development, I wanted to explore the power of javascript... Thanks to Ryan Dahl for developing a great nodejs platform. At the end of 2022, I read about a relatively recent front-end component...</p>
        </div>
        <div> 
            <h1 class="text-white font-bold">#2023</h1>
            <p class="text-sm text-gray-500 dark:text-gray-400">After delving into the development of websites and seeing the latest technologies, svelte caught my eye. It is really great, light and easy to learn. At the end of 2022, sveltekit was officially released and since then I started using it in many projects (this site is built through it. Do you like it? View the <a href="https://github.com/omarammura-dev/Personal-Portfolio" class="font-bold text-cyan-400 hover:text-green-600">code on GitHub</a> ).</p>
        </div>
      </div>
      <div class="py-10 ">
            <Badge>JavaScript</Badge>
            <Badge color="dark">PHP</Badge>
            <Badge color="red">SvelteJs</Badge>
            <Badge color="green">NodeJs</Badge>
            <Badge color="yellow">MongoDB</Badge>
            <Badge color="indigo">SvelteKit</Badge>
            <Badge color="purple">Tailwind</Badge>
            <Badge color="pink">ExpressJs</Badge>
      </div>
     </TabItem>
    
     <TabItem  title="Android Development" >
        <div class="grid gap-4 grid-cols-2 grid-rows-1">
            <div class="">
                <h1 class="text-white font-bold">#2021</h1>
                <p class="text-sm text-gray-500 dark:text-gray-400">I've always been amazed at some Android apps...the design, the way it works, the effort, etc. I wanted to take a new curve in my path, and from here I went to the development of Android applications. I started to learn the Java language from some famous courses on the Internet. During my learning, I was reading some articles that criticized Java because of the way of writing and so on. In fact, some of the articles affected me... But after digging deeper and seeing how powerful Java is, I changed my mind. I learned to deal with different databases in general and Firebase in particular. Firebase has always made the task easier for me through the wonderful additions and features provided by Google.</p>
            </div>
            <div class="">
                <h1 class="text-white font-bold">#2023</h1>
                <p class="text-sm text-gray-500 dark:text-gray-400">We are in 2023 now... I am still trying to develop myself and delve into the massive Java language and develop open source applications and projects. I wanted to build apps on the Ios platform, but unfortunately I couldn't because I didn't have MacOS. However, I am now learning Dart to target more platforms in less time (I use flutter for intermediate applications). My career continues...</p>
            </div>
          </div>
          <div class="py-10 ">
                <Badge>Java</Badge>
                <Badge color="dark">Firebase</Badge>
                <Badge color="red">Kotlin</Badge>
                <Badge color="green">XML</Badge>
                <Badge color="yellow">RealtimeDB</Badge>
                <Badge color="purple">Flutter</Badge>
          </div>
     </TabItem>
     <TabItem  title="AI" >
        <div class="grid gap-4 grid-cols-2 grid-rows-1">
            <div class="">
                <h1 class="text-white font-bold">#2022</h1>
                <p class="text-sm text-gray-500 dark:text-gray-400">My interest in artificial intelligence and automation began to increase, especially after participating in a competition organized by the Scientific and Technological Research Council in Turkey. In short, it is a competition between high schools in Turkey, Azerbaijan and Northern Cyprus aimed at making a drone with an automatic system.</p>
            </div>
            <div class="">
                <h1 class="text-white font-bold">#2023</h1>
                <p class="text-sm text-gray-500 dark:text-gray-400">After seeing sites like ChatGPT and bard, I started researching and learning neural networks and deep learning. I used the Python language with famous libraries such as Tensorflow and Pytorch. So far, I am not a professional, but I am still learning and my career continues...</p>
            </div>
          </div>
          <div class="py-10 ">
                <Badge>Python</Badge>
                <Badge color="dark">Tensorflow</Badge>
                <Badge color="red">Pytorch</Badge>
                <Badge color="green">numpy</Badge>
          </div>
     </TabItem>
     <TabItem  title="Competitive Programming" >
        <div class="justify-center">
            <div class="">
                <h1 class="text-white font-bold">#Zero To Hero</h1>
                <p class="text-sm text-gray-500 dark:text-gray-400">From the beginning, programming competitions interested me... I participated in the first local competition held between high schools in 2021. I didn't score well enough... but this is only the beginning. In the world of 2022, I did not have enough opportunities to continue to develop because of the university exam. Now I am developing myself in this field. Now i have good rating on CoderForces,CodeChef and other websites</p>
            </div>
            
          </div>
          <div class="py-10 ">
                <Badge>C++</Badge>
                <Badge color="dark">Data Structures</Badge>
                <Badge color="red">Algorithms</Badge>
                <Badge color="green">Java</Badge>
          </div>
     </TabItem>
</Tabs>



<style>
    @media screen and (max-width: 640px) {
    .grid-cols-responsive {
      grid-template-columns: repeat(2, 1fr);
    }
  }

</style>