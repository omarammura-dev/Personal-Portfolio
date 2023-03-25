<script>
     import { Timeline, TimelineItem } from 'flowbite-svelte';
    export let experinces;
</script>

<Timeline>
   {#each experinces as experince }
   <TimelineItem title="{experince.title}" date="{experince.date}">
    <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">{experince.p}</p>
  </TimelineItem>
   {/each}
  </Timeline>