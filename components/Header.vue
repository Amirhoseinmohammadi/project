<template>
   <div class=" relative  ">
    <div class="navbar bg-base-200 text-base-content hidden sm:flex gap-4 md:flex lg:flex xl:flex ">
  <div class="navbar-start">
    
     <button class="btn btn-ghost btn-circle  "  >
      <div class="indicator">
        <label for="my-modal-3" >  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 " fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9" /></svg></label>
        <span class="badge badge-xs   bg-warning  border-warning indicator-item  " ></span>
      </div>
    </button>
 
<input type="checkbox" id="my-modal-3" class="modal-toggle" />
<div class="modal">
  <div class="modal-box relative">
    <label for="my-modal-3" class="btn btn-sm btn-warning btn-circle absolute right-2 top-2 ">✕</label>
    <h3 class="text-lg font-bold">Congratulations random Internet user!</h3>
    <p class="py-4">You've been selected for a chance to get one year of subscription to use Wikipedia for free!</p>
  </div>
</div>
    
  </div>
  <div class="navbar-center">
   <ul>
        <li>
          


          <NuxtLink
          
          class=" text-lg  px-5 p-2 mx-2 shadow bg-sky-400  hover:bg-sky-300  rounded-2xl  hover:text-black   "
          v-for="({text,route},index) in links" 
          :key="index"
          :to="route"
          
          >
        
        {{text}}
        </NuxtLink>

    
        
        </li>
      </ul>

        
     
    
  </div>
 
  <div class="navbar-end">
    <button class="btn btn-ghost btn-circle">
      <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" /></svg>
    </button>
   
  </div>
</div>

<div class=" m-5 flex  justify-between sm:hidden md:hidden lg:hidden xl:hidden 2xl:hidden bg-base-200 rounded-md">
 

  <div class="dropdown dropdown-right mb-2 ">
  <label tabindex="0" class="btn btn-info mt-2 ml-2 shadow-lg">
    <svg  class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M4 6h16M4 12h16M4 18h16" /></svg>

  </label>
 <div>
  <ul tabindex="0" class="dropdown-content menu p-3 shadow bg-base-100 rounded-box  w-fit ml-3 ">
   
    
   <li>
     


     <NuxtLink
     
     class="   "
     v-for="({text,route},index) in links" 
     :key="index"
     :to="route"
     
     >
    
       {{text}}
     
   
   
   </NuxtLink>


   
   </li>
 </ul>
 </div>
 
</div>


<div class="dropdown dropdown-left mb-2 shadow-lg ">
  <label tabindex="0" class=" btn btn-info  mt-2 mr-2 ">
    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" /></svg>

  </label>
  <ul tabindex="0" class="dropdown-content menu p-2 shadow bg-base-100 rounded-box    w-40  ">
    <input type="text" placeholder="Type here" class="input input-bordered  input-warning  w-full max-w-xs " />
  </ul>
</div>


</div>

   </div> 
   
</template>
<script setup>

const links = ref([

{text:"Home",route:"/"},
{text:"Portfolio",route:"/Portfolio"},
{text:"About",route:"/About"}


]);


</script>