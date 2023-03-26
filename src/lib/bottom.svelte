<script>
 import { BottomNav, BottomNavItem ,Tooltip} from "flowbite-svelte"
</script>
  


<BottomNav position="fixed" navType="application" innerDiv="grid-cols-4" outerClass="bg-green-600">
 
    <BottomNavItem btnName="Home" appBtnPosition="left">
      <svg class="w-6 h-6 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-green-600 dark:group-hover:text-green-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <path d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"></path>
      </svg>
      <Tooltip arrow={false}>Home</Tooltip>
  </BottomNavItem>



  <BottomNavItem btnName="Experinces" appBtnPosition="middle">
      <svg class="w-6 h-6 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-green-600 dark:group-hover:text-green-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <path d="M5 4a1 1 0 00-2 0v7.268a2 2 0 000 3.464V16a1 1 0 102 0v-1.268a2 2 0 000-3.464V4zM11 4a1 1 0 10-2 0v1.268a2 2 0 000 3.464V16a1 1 0 102 0V8.732a2 2 0 000-3.464V4zM16 3a1 1 0 011 1v7.268a2 2 0 010 3.464V16a1 1 0 11-2 0v-1.268a2 2 0 010-3.464V4a1 1 0 011-1z"></path>
      </svg>
    <Tooltip arrow={false}>Experinces</Tooltip>
  </BottomNavItem>
  <BottomNavItem btnName="Contact" appBtnPosition="right">
      <svg class="w-6 h-6 mb-1 text-gray-500 dark:text-gray-400 group-hover:text-green-600 dark:group-hover:text-green-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <path clip-rule="evenodd" fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.084A5 5 0 0010 11z"></path>
      </svg>
      <Tooltip arrow={false}>Contact</Tooltip>
  </BottomNavItem>
</BottomNav>  