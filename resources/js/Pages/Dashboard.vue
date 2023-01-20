<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/inertia-vue3';
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">Dashboard</h2>
        </template>
        
        <!-- component -->

<div class="container mx-auto my-5 w-100">

<div class="relative  flex flex-col md:flex-row items-center md:shadow-xl md:h-72 mx-2">
    
    <div class="z-0 order-1 relative w-full md:w-2/5 h-80 md:h-full overflow-hidden rounded-lg md:rounded-none md:rounded-r-lg">
            <div class="absolute inset-0 w-full h-full object-fill object-center bg-blue-400 bg-opacity-30 bg-cover bg-bottom" style="background-image: url(../img/profile.jpeg ); background-blend-mode: multiply;"></div>
            <div class="md:hidden absolute inset-0 h-full p-6 pb-6 flex flex-col-reverse justify-start items-start bg-gradient-to-b from-transparent via-transparent to-gray-900">
                
            </div>           
        </div>

    <div class="z-10 order-2  w-full h-full flex items-center ">
        <div class="p-8 md:pr-18 md:pl-14 md:py-12 mx-2 md:mx-0 h-full w-full bg-white">
            <h2 class="hidden md:block text-xl text-black-400 font-bold">  {{ $page.props.auth.user.name }}</h2>      
            <h4 class="hidden md:block text-l text-black-400">  Bio </h4>          
            <p class="text-gray-600 text-justify"> {{ $page.props.auth.user.bio }} dsaaaaaaaaaadsadsadasdasdsadasdaaaaaaaaaaaaaaaaaaa</p>            
        </div>
    </div>

    <div class="z-10 order-3  w-full h-full  flex items-center ">
        <div class="w-100 p-8 md:pr-18 md:pl-14 md:py-12 mx-2 md:mx-0 h-full bg-white rounded-lg md:rounded-none md:rounded-l-lg shadow-xl md:shadow-none">               
            <p class="text-gray-600 text-justify"> <b>Phone:</b> <br/>{{ $page.props.auth.user.phone }} </p>          
            <p class="text-gray-600 text-justify"> <b>Email:</b><br/>{{ $page.props.auth.user.email }}</p>            
        </div>
    </div>
    
</div>

<section class="overflow-hidden text-gray-700 ">
  <div class="container px-5 py-2 mx-auto lg:pt-12 lg:px-32">
    <div class="flex flex-wrap -m-1 md:-m-2">
      <div class="flex flex-wrap w-1/3">
        <div class="w-full p-1 md:p-2">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src="../img/landscape1.jpeg">
        </div>
      </div>
      <div class="flex flex-wrap w-1/3">
        <div class="w-full p-1 md:p-2">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src="../img/landscape2.jpeg">
        </div>
      </div>
      <div class="flex flex-wrap w-1/3">
        <div class="w-full p-1 md:p-2">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src="../img/landscape3.jpeg">
        </div>
      </div>
      <div class="flex flex-wrap w-1/3">
        <div class="w-full p-1 md:p-2">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src="../img/landscape4.jpeg">
        </div>
      </div>
      <div class="flex flex-wrap w-1/3">
        <div class="w-full p-1 md:p-2">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src="../img/landscape5.jpeg">
        </div>
      </div>
      <div class="flex flex-wrap w-1/3">
        <div class="w-full p-1 md:p-2">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src="../img/landscape6.jpeg">
        </div>
      </div>
    </div>
  </div>
</section>
</div>

        
    </AuthenticatedLayout>
</template>

<script>
import userData from '../landscapes.json'
export default {
  data() {
    return {
      users: userData,
    };
  },
};
</script>