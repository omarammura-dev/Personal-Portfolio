<script>
    import { Alert, Input, Label } from 'flowbite-svelte';
    import { Textarea } from 'flowbite-svelte'
    import Card from './card.svelte'
    import { onMount } from 'svelte';

    let name = "";
    let surname = "";
    let email = "";
    let message = "";
    let visible = false;
    let error = false;
    let recaptchaToken = "";

    onMount(() => {
        window.onRecaptchaLoad = () => {
            grecaptcha.render('recaptcha', {
                'sitekey': '6LdOltAUAAAAAAZ7ir28BZGban9Wj6IfahD45BUW',
                'callback': (token) => { recaptchaToken = token; }
            });
        }
    });

    function toggleVisible() {
        visible = !visible
    } 

    const endpoint = 'http://api.mux04.com/graphql'
    
    async function doPost() {
        if (!recaptchaToken) {
            error = true;
            return;
        }

        try {
            const res = await fetch(endpoint, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({
                    query: `
                    mutation {
                      createContact(contact:{
                        name: "${name} ${surname}",
                        email: "${email}",
                        message: "${message}",
                        from: "main"
                      })
                      {
                        id
                      }
                    }
                    `
                })
            })
            if (res.status === 200) {
                toggleVisible();
            } else {
                error = true;
            } 
            const json = await res.json()
            result = JSON.stringify(json)
        } catch (err) {
            console.error(err)
            error = true;
        }
    
        name = "";
        surname = "";
        email = "";
        message = "";
        grecaptcha.reset();
    }
</script>

<svelte:head>
    <script>
        let recaptchaLoaded = false;
        function onRecaptchaLoad() {
            if (!recaptchaLoaded) {
                recaptchaLoaded = true;
                if (typeof window.onRecaptchaLoad === 'function') {
                    window.onRecaptchaLoad();
                }
            }
        }
    </script>
    <script src="https://www.google.com/recaptcha/api.js?onload=onRecaptchaLoad&render=explicit" async defer></script>
</svelte:head>

<div class="flex justify-center">
    <div>   
        <Card/> 
    </div>
    <div class="px-20">
        <form on:submit|preventDefault={doPost} method="post">
            <div class="grid gap-6 mb-6 md:grid-cols-2">
                <div>
                    <Label for="first_name" class="mb-2 text-gray-900">First name</Label>
                    <Input type="text" id="first_name" class="bg-slate-800 border-gray-200" bind:value={name} placeholder="John" required />
                </div>
                <div>
                    <Label for="last_name" class="mb-2">Last name</Label>
                    <Input type="text" id="last_name" class="bg-slate-800 border-gray-200" bind:value={surname} placeholder="Doe" required />
                </div>
            </div>
            <div class="mb-6">
                <Label for="email" class="mb-2">Email address</Label>
                <Input type="email" id="email" class="bg-slate-800 border-gray-200" bind:value={email} placeholder="john.doe@company.com" required />
            </div>
            <div class="mb-6">
                <Label for="message" class="mb-2 h-5">Your Message</Label>
                <Textarea id="message" bind:value={message} class="bg-slate-800 border-gray-200" placeholder="Your message" rows="4" name="message"/>
            </div>
            <div class="mb-6">
                <div id="recaptcha"></div>
            </div>
            <button type="submit" class="mx-auto relative inline-flex items-center justify-center p-0.5 mb-2 mr-2 overflow-hidden text-sm font-medium text-gray-900 rounded-lg group bg-gradient-to-br from-green-400 to-blue-600 group-hover:from-green-400 group-hover:to-blue-600 hover:text-white dark:text-white focus:ring-4 focus:outline-none focus:ring-green-200 dark:focus:ring-green-800">
                <span class="mx-auto justify-center relative px-5 py-2.5 transition-all ease-in duration-75 bg-white dark:bg-gray-900 rounded-md group-hover:bg-opacity-0">
                    Submit
                </span>
            </button> 
            {#if visible}
                <Alert color="green">
                    <span class="font-medium">Success!</span> Your message has been sent.
                </Alert>
            {/if}
            {#if error && !visible}
                <Alert color="red">
                    <span class="font-medium">Error!</span> Oops! Something went wrong.
                </Alert>
            {/if}
        </form>
    </div>
</div>

<style>
   @media screen and (max-width: 640px) {
    .flex {
      flex-direction: column;
      align-items: center;
    }
    .px-20 {
      padding-left: 2rem;
      padding-right: 2rem;
    }
    .grid {
      grid-template-columns: 1fr;
    }
  }
</style>
