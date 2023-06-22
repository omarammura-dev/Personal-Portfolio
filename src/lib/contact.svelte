<script>
    import { Alert, Input, Label } from 'flowbite-svelte';
    import { Textarea } from 'flowbite-svelte'
    import Card from './card.svelte'
		// getting the action url
    let name = "";
    let surname = "";
    let email = "";
    let message = "";
    let visible = false;

  function toggleVissible() {
    visible = !visible
    } 
		const ACTION_URL = 'https://send.pageclip.co/vOf1aijihVi3PCuBhDN1lJQ7VyLSmvuD/myWebsite'

    async function doPost () {
		const res = await fetch(ACTION_URL, {
			method: 'POST',
			body: JSON.stringify({
				name,
				surname,
        email,
        message
			})
    
		})
     name = "";
      surname = "";
      email = "";
      message = "";
      toggleVissible();
		const json = await res.json()
		result = JSON.stringify(json)
    
	}
</script>

<div class="flex justify-center">
  <div>   
    <Card/> 
  </div>
<div class="px-20">

<form  on:submit|preventDefault={doPost} method="post">
    <div class="grid  gap-6 mb-6 md:grid-cols-2">
      <div>
        <Label for="first_name" class="mb-2">First name</Label>
        <Input type="text" id="first_name" bind:value={name} placeholder="John" required  />
      </div>
      <div>
        <Label for="last_name" class="mb-2">Last name</Label>
        <Input type="text" id="last_name" bind:value={surname} placeholder="Doe" required />
      </div>
    </div>
    <div class="mb-6">
      <Label for="email" class="mb-2">Email address</Label>
      <Input type="email" id="email" bind:value={email} placeholder="john.doe@company.com" required />
    </div>
    <div class="mb-6">
        <Label for="message" class="mb-2 h-5">Your Message</Label>
        <Textarea id="message" bind:value={message} placeholder="Your message" rows="4" name="message"/>
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

