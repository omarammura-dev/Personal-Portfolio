<script>
    import { Tabs, TabItem } from 'flowbite-svelte';
    import { Badge } from 'flowbite-svelte';
    export let tabs;
</script>

<Tabs class="justify-center">
    <TabItem  open title="Web development" color="green">
        <p class="text-sm text-gray-500 dark:text-gray-400">text for Web</p>
     </TabItem>
    {#each tabs as tab }
     <TabItem  title="{tab.title}" >
        <p class="text-sm text-gray-500 dark:text-gray-400">{tab.p}</p>
     </TabItem>
    {/each}
    
</Tabs>



