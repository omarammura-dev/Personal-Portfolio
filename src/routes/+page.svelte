<script>
    import Head from '$lib/header.svelte'
    import Footer from '$lib/footer.svelte'
    import Tab from '$lib/tab.svelte'
    import Contact from '$lib/contact.svelte'
    import Experinces from '../lib/experinces.svelte';
    import { Hr,Img,Blockquote, Card, Accordion, AccordionItem } from 'flowbite-svelte'
   

    let experinces= [{title:"Goodright GmbH (Pflegewächter), Full Stack Developer",date:"2023-present",p:"Responsible of the development for company's system"},{title:"MYRC L.L.C. (Remotely-Oman), General Developer ",date:"2022-2023",p:"Responsible for managing the company's website server and creating web and Android applications. Also responsible for troubleshooting."},
    {title:"SANA Group (Remotely-Saudi Arabia), Web developer",date:"2023",p:"Develop and design Shopping website"},{title:"Android Develoeper (Freelance)",date:"2021",p:"Building Native Android Chat Application "}]

   
</script>


<Head/>
<div class="container mx-auto flex flex-col my-4 mt-10 w-full">
  <section class="full-screen d-flex justify-content-center align-items-center">
    <ul class="circles">
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
    </ul>
    <div class="content">
      <div>
        <img class="rounded-full w-60 h-60 mx-auto" src="/main-image.jpg" alt="MyImage">
        <h5 class="mb-4 text-xl text-center font-extrabold text-gray-900 dark:text-white md:text-1xl pt-7 lg:text-3xl">Hello, I'm</h5>
        <h1 class="mb-4 text-3xl text-center font-extrabold text-gray-900 text-white md:text-5xl lg:text-6xl"><span class="text-transparent bg-clip-text bg-gradient-to-r to-emerald-600 from-sky-400">Omar Ammura</span></h1>
        <p class="text-lg font-normal text-gray-500 lg:text-xl text-gray-400 text-center">Computer Engineering Student</p>
        <p class="text-lg font-normal text-gray-500 lg:text-xl text-gray-400 text-center mb-8">Full Stack Developer at Goodright GmbH (Pflegewächter)</p>
      </div>
      <div class="buttons">
        <a href="/MyResume.pdf">
          <button class="relative inline-flex items-center justify-center p-0.5 mb-2 mr-2 overflow-hidden text-sm font-medium text-gray-900 rounded-lg group bg-gradient-to-br from-green-400 to-blue-600 group-hover:from-green-400 group-hover:to-blue-600 hover:text-white dark:text-white focus:ring-4 focus:outline-none focus:ring-green-200 dark:focus:ring-green-800">
            <span class="justify-center relative px-5 py-2.5 transition-all ease-in duration-75 bg-white dark:bg-gray-900 rounded-md group-hover:bg-opacity-0">
              Download CV
            </span>
          </button>
        </a>
        <a href="#Contact">
          <button href="" class="mx-auto relative inline-flex items-center justify-center p-0.5 mb-2 mr-2 overflow-hidden text-sm font-medium text-gray-900 rounded-lg group bg-gradient-to-br from-green-400 to-blue-600 group-hover:from-green-400 group-hover:to-blue-600 hover:text-white dark:text-white focus:ring-4 focus:outline-none focus:ring-green-200 dark:focus:ring-green-800">
            <span class="mx-auto justify-center relative px-5 py-2.5 transition-all ease-in duration-75 bg-white dark:bg-gray-900 rounded-md group-hover:bg-opacity-0">
              Contact me
            </span>
          </button> 
        </a>
       
      </div>
    </div>
    <div class="scroll-indicator">
      <svg fill="#31C48D" class="animate-bounce" height="35px" width="35px" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 512.04 512.04" xml:space="preserve">
        <g>
          <g>
            <path d="M508.933,146.807l-42.347-42.347c-4.267-4.053-10.88-4.053-15.147,0L256.027,300.193L60.507,104.46
              c-4.267-4.053-10.88-4.053-15.147,0L3.12,146.807c-4.16,4.16-4.16,10.88,0,15.04L248.453,407.5c4.16,4.16,10.88,4.16,15.04,0
              l245.333-245.653C513.093,157.687,513.093,150.967,508.933,146.807z M256.027,384.887L25.733,154.38l27.2-27.307l195.52,195.733
              c4.267,4.053,10.88,4.053,15.147,0l195.52-195.733l27.2,27.307L256.027,384.887z"/>
          </g>
        </g>
      </svg>
    </div>
  </section>
    <div id="About">
        <h1 class=" text-7xl py-5 font-extrabold text-white text-center mt-20 font-serif">About me</h1>
        <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 dark:bg-gray-700">
    </div>
    <section>
       <div class="flow-root" >
        <div class="float-left round-lg bg-green-600 w-60 mx-10 flex-auto" style=" max-width: 100%;flex-basis: 40%">
            <Img src="about-image.png" alt="" class="rounded-md rotate-6 hover:rotate-0 w-60"  figClass="relative max-w-sm transition-all duration-300 cursor-pointer filter grayscale hover:grayscale-0" captionClass="absolute bottom-6 px-4 text-lg text-white" caption="Would you like to know about me ?" />
        </div>
        <div class="px-20 justify-end text-white">
            <Blockquote size='md' >
                <svg aria-hidden="true" class="w-10 h-10 flex-auto text-gray-400 text-gray-600" viewBox="0 0 24 27" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M14.017 18L14.017 10.609C14.017 4.905 17.748 1.039 23 0L23.995 2.151C21.563 3.068 20 5.789 20 8H24V18H14.017ZM0 18V10.609C0 4.905 3.748 1.038 9 0L9.996 2.151C7.563 3.068 6 5.789 6 8H9.983L9.983 18L0 18Z" fill="currentColor"/></svg>
          <p class="text-white">
            Hi there! I'm a Computer Engineering student who has been passionate about programming since 2019. I discovered my love for coding when I started learning about Web Development, and I have been hooked ever since.<br/>

            What I enjoy most about programming is the ability to create something out of nothing, and the thrill of seeing my code come to life. As a naturally curious person, I love learning new things, and programming allows me to do just that. With every project, I am always eager to expand my knowledge and skills, and I am constantly seeking out new challenges to push myself further.<br/>
            
            In addition to programming, I am also interested in exploring other areas of computer engineering, such as hardware design and networking. I believe that having a well-rounded understanding of all aspects of computing is essential for becoming a successful engineer,and I am eager to explore all that this field has to offer.<br/>
            In my free time, I enjoy participating in coding competitions and hackathons, where I can test my skills and learn from other developers. I am also a regular contributor to open-source projects, as I believe that sharing knowledge and resources is essential for the growth and development of the programming community.<br/>

 As a Computer Engineering student, I am currently focusing on developing my skills in software engineering, data structures and algorithms, and web development. I am also exploring new areas of programming, such as machine learning and artificial intelligence, to stay up-to-date with the latest trends and advancements in the field.<br/>
            
            As I continue my journey as a Computer Engineering student, I am excited to see where my passion for programming and learning will take me. I am always looking for new opportunities to expand my skills and knowledge, and I am eager to contribute my expertise to meaningful projects and initiatives. 
          </p>
                <svg aria-hidden="true" class="w-10 h-10 flex-auto rotate-180 justify-end text-gray-400 text-gray-600" viewBox="0 0 24 27" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M14.017 18L14.017 10.609C14.017 4.905 17.748 1.039 23 0L23.995 2.151C21.563 3.068 20 5.789 20 8H24V18H14.017ZM0 18V10.609C0 4.905 3.748 1.038 9 0L9.996 2.151C7.563 3.068 6 5.789 6 8H9.983L9.983 18L0 18Z" fill="currentColor"/></svg>
      
            </Blockquote>
        </div>
       </div>
    </section>
<!-- <div id="Skills">
    <h1 class="text-7xl py-5 font-extrabold text-white text-center mt-20 font-serif">Skills</h1>
    <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 bg-gray-700">
</div>
    <section class="bg-slate-800">
        <Tab/> 
    </section> -->

    <div id="L&T">
        <h1 class=" text-7xl py-5 font-extrabold dark:text-white text-white text-center mt-20 font-serif">Languages & Tools</h1>
        <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 bg-gray-700">
    </div>
    <script>
      import { Card, List, Li, Accordion, AccordionItem } from 'flowbite-svelte';
    </script>
    <section class="py-12 bg-slate-800">
      <div class="container mx-auto px-4">
        <div class="flex flex-col items-center">
          <Card class="w-full max-w-3xl mb-8">
            <h5 class="mb-4 text-2xl font-bold tracking-tight text-gray-900 dark:text-white text-center">Programming Languages</h5>
            <div class="flex flex-wrap justify-center gap-4">
              {#each ['Go','C++', 'Java', 'Kotlin', 'Python', 'TypeScript'] as language}
                <span class="px-4 py-2 bg-blue-500 text-white rounded-full">{language}</span>
              {/each}
            </div>
          </Card>
          <Card class="w-full max-w-3xl">
            <h5 class="mb-4 text-2xl font-bold tracking-tight text-gray-900 dark:text-white text-center">Technologies & Tools</h5>
            <Accordion>
              <AccordionItem>
                <span slot="header">Frameworks, Libraries & Runtime</span>
                <div class="flex flex-wrap justify-center gap-4 mt-2">
                  {#each ['Quarkus','Node.js', 'Svelte','React','Angular', 'Express.js', 'GraphQL'] as framework}
                    <span class="px-4 py-2 bg-green-500 text-white rounded-full">{framework}</span>
                  {/each}
                </div>
              </AccordionItem>
              <AccordionItem>
                <span slot="header">DevOps</span>
                <div class="flex flex-wrap justify-center gap-4 mt-2">
                  {#each ['Docker', 'Git', 'CI/CD'] as tool}
                    <span class="px-4 py-2 bg-red-500 text-white rounded-full">{tool}</span>
                  {/each}
                </div>
              </AccordionItem>
              <AccordionItem>
                <span slot="header">Cloud Platforms</span>
                <div class="flex flex-wrap justify-center gap-4 mt-2">
                  {#each ['Azure', 'Google Cloud', 'AWS'] as platform}
                    <span class="px-4 py-2 bg-purple-500 text-white rounded-full">{platform}</span>
                  {/each}
                </div>
              </AccordionItem>
              <AccordionItem>
                <span slot="header">Databases</span>
                <div class="flex flex-wrap justify-center gap-4 mt-2">
                  {#each ['MySQL / SQLite', 'MongoDB', 'Firebase'] as database}
                    <span class="px-4 py-2 bg-yellow-500 text-white rounded-full">{database}</span>
                  {/each}
                </div>
              </AccordionItem>
            </Accordion>
          </Card>
        </div>
      </div>
    </section>
    <div id="Experince">
        <h1 class="text-7xl py-5 font-extrabold text-white text-center mt-20 font-serif">Experiences</h1>
        <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 dark:bg-gray-700">
    
    </div>    
    <Experinces {experinces}/>

    <!-- <div id="Testimonial">
      <h1 class=" text-7xl py-5 font-extrabold text-white text-center mt-20 font-serif">Testimonial</h1>
      <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 dark:bg-gray-700">
  </div>
  <section>
     <div class="flow-root" >
      <Testimonial/>
     </div>
  </section> -->
    <div id="Contact">
        <h1 class="text-7xl py-5 font-extrabold text-white text-center mt-20 font-serif">Contact Me</h1>
        <hr class="w-48 h-1 mx-auto my-4 bg-gray-100 border-0 rounded md:my-10 dark:bg-gray-700">
    </div>    
    <section>
       <Contact/>
    </section>
    <Hr class="my-5" height="h-px" />

<div class="flex">
    <div class="flex-1">
        <Footer/> 
    </div>
    <div>
        <a href="/">
            <div class="flex-1 rotate-180 w-25 h-25 my-5" >
                <svg fill="#31C48D" class="animate-bounce" height="25px" width="25px" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
                viewBox="0 0 512.04 512.04" xml:space="preserve">
                   <g>
               <g>
                   <path d="M508.933,146.807l-42.347-42.347c-4.267-4.053-10.88-4.053-15.147,0L256.027,300.193L60.507,104.46
                       c-4.267-4.053-10.88-4.053-15.147,0L3.12,146.807c-4.16,4.16-4.16,10.88,0,15.04L248.453,407.5c4.16,4.16,10.88,4.16,15.04,0
                       l245.333-245.653C513.093,157.687,513.093,150.967,508.933,146.807z M256.027,384.887L25.733,154.38l27.2-27.307l195.52,195.733
                       c4.267,4.053,10.88,4.053,15.147,0l195.52-195.733l27.2,27.307L256.027,384.887z"/>
               </g>
           </g>
           </svg>
              </div>
        </a>
    </div>
</div> 
</div> 

<style>
  @media (prefers-color-scheme: dark) or (prefers-color-scheme: no-preference),
(prefers-color-scheme: light) {
 
}
.circles {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    overflow: hidden;
    z-index: -1;
}

@media (max-width: 768px) {
    .circles {
        position: fixed;
    }
}

.circles li {
    position: absolute;
    display: block;
    list-style: none;
    width: 20px;
    height: 20px;
    background: rgba(255, 255, 255, 0.2);
    animation: animate 25s linear infinite;
    bottom: -150px;
}

.circles li:nth-child(1) {
    left: 25%;
    width: 80px;
    height: 80px;
    animation-delay: 0s;
}

.circles li:nth-child(2) {
    left: 10%;
    width: 20px;
    height: 20px;
    animation-delay: 2s;
    animation-duration: 12s;
}

.circles li:nth-child(3) {
    left: 70%;
    width: 20px;
    height: 20px;
    animation-delay: 4s;
}

.circles li:nth-child(4) {
    left: 40%;
    width: 60px;
    height: 60px;
    animation-delay: 0s;
    animation-duration: 18s;
}

.circles li:nth-child(5) {
    left: 65%;
    width: 20px;
    height: 20px;
    animation-delay: 0s;
}

.circles li:nth-child(6) {
    left: 75%;
    width: 110px;
    height: 110px;
    animation-delay: 3s;
}

.circles li:nth-child(7) {
    left: 35%;
    width: 150px;
    height: 150px;
    animation-delay: 7s;
}

.circles li:nth-child(8) {
    left: 50%;
    width: 25px;
    height: 25px;
    animation-delay: 15s;
    animation-duration: 45s;
}

.circles li:nth-child(9) {
    left: 20%;
    width: 15px;
    height: 15px;
    animation-delay: 2s;
    animation-duration: 35s;
}

.circles li:nth-child(10) {
    left: 85%;
    width: 150px;
    height: 150px;
    animation-delay: 0s;
    animation-duration: 11s;
}

@media screen and (max-width: 640px) {
    .circles {
        right: 20px; /* Add right margin for mobile screens */
    }
}



@keyframes animate {
    0%{
        transform: translateY(0) rotate(0deg);
        opacity: 1;
        border-radius: 0;
    }

    100%{
        transform: translateY(-1000px) rotate(720deg);
        opacity: 0;
        border-radius: 50%;
    }

}
@media screen and (max-width: 640px) {
    .float-left {
      float: none;
      margin-left: 0;
    }
    .mt-10 {
      margin-top: 2rem;
    }
    .my-4 {
      margin-top: 1rem;
      margin-bottom: 1rem;
    }
  
  }

  .full-screen {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 0;
  }

  .content {
    text-align: center;
    margin-bottom: 2rem;
  }

  .buttons {
    display: flex;
    justify-content: center;
    margin-bottom: 2rem;
  }

  .scroll-indicator {

    text-align: center;
  }


</style>
        

