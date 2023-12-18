<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
   <div class="container-fluid">
     <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
       <span class="navbar-toggler-icon"></span>
     </button>
     <div class="collapse navbar-collapse" id="navbarSupportedContent">
       <ul class="navbar-nav me-auto mb-2 mb-lg-0">
         <li class="nav-item" v-for="(navItem, i) in navBarItems" :key="`nav-item-${i+1}`" @click="onChangeActiveNav(navItem.link)">
           <a class="nav-link" :class="{ 'active': navItem.isActive }" aria-current="page" href="#">{{ navItem.name }}</a>
         </li>
       </ul>
     </div>
   </div>
 </nav>
 </template>
 
 <script>
 
 export default {
   name: 'HelloWorld',
   props: {
     navBarItems: Array
   },
   methods: {
     onChangeActiveNav (navItemLink) {
       this.$emit('on-change-active-nav', navItemLink)
     }
   }
 }
 </script>
 
 <style scoped>
 .nav-link.active {
   font-weight: bold;
 }
 </style>
 