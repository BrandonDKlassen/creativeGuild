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
    
    <div class="z-0 order-1 relative w-full">
        <div class="img src: storage/app/public/images/profile.jpeg;"></div>
        <div class="md:hidden absolute inset-0 h-full p-6 pb-6 flex flex-col-reverse justify-start items-start bg-gradient-to-b from-transparent via-transparent to-gray-900">
            <h3 class="w-full font-bold text-2xl text-white leading-tight mb-2">HOTEL AMANEE</h3>
            <h4 class="w-full text-xl text-gray-100 leading-tight">Bienvenido a</h4>
        </div>
        <svg class="hidden md:block absolute inset-y-0 h-full w-24 fill-current text-white -ml-12" viewBox="0 0 100 100" preserveAspectRatio="none">
            <polygon points="50,0 100,0 50,100 0,100" />
        </svg>
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
</div>

        
    </AuthenticatedLayout>
</template>
