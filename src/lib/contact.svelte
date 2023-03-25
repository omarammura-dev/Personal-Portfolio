<script>
    import { Input, Label } from 'flowbite-svelte';
    import { Button } from 'flowbite-svelte';
    import { Textarea } from 'flowbite-svelte'
    const handleSubmit = e => {
		// getting the action url
		const ACTION_URL = e.target.action

		// get the form fields data and convert it to URLSearchParams
		const formData = new FormData(e.target)
		const data = new URLSearchParams()
		for (let field of formData) {
			const [key, value] = field
			data.append(key, value)
		}

        if (e.target.method.toLowerCase() == 'get') fetch(`${ACTION_URL}?${data}`)
		else {
			fetch(ACTION_URL, {
				method: 'POST',
				body: data
			})			
		}			
		
	}
</script>



    <form  on:submit|preventDefault={handleSubmit} action="https://send.pageclip.co/vOf1aijihVi3PCuBhDN1lJQ7VyLSmvuD/myWebsite">
        <div class="grid  gap-6 mb-6 md:grid-cols-2">
          <div>
            <Label for="first_name" class="mb-2">First name</Label>
            <Input type="text" id="first_name" placeholder="John" required  />
          </div>
          <div>
            <Label for="last_name" class="mb-2">Last name</Label>
            <Input type="text" id="last_name" placeholder="Doe" required />
          </div>
        </div>
        <div class="mb-6">
          <Label for="email" class="mb-2">Email address</Label>
          <Input type="email" id="email" placeholder="john.doe@company.com" required />
        </div>
        <div class="mb-6 ">
            <Label for="message" class="mb-2 h-5">Your Message</Label>
            <Textarea id="message" placeholder="Your message" rows="4" name="message"/>
          </div>
          <Button type="submit">Submit</Button>
      </form>

