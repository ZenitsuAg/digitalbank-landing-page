<script setup>
import { ref } from 'vue';
import logoDark from '../../images/logo-dark.svg'
import hamburger from '../../images/icon-hamburger.svg'
import iconClose from '../../images/icon-close.svg'
import gsap from 'gsap'

const openMenu = ref(false)

function onBeforeEnter(el) {
    gsap.set(el, {
        y: -50,
        ease: 'power.inOut(2.5, 1)',
        opacity: 1
    })
}

function onEnter(el, done) {
    gsap.to(el, {
        y: 64,
        duration: 0.5,
        scaleX: 1,
        scaleY: 1,
        opacity: 1,
        ease: 'power.inOut(2.5, 1)',
        onComplete: done
    })
}

function onLeave(el, done) {
    gsap.to(el, {
        duration: 0.7,
        scaleX: 1,
        scaleY: 1,
        y: -700,
        ease: 'power.inOut(2.5, 1)'
    })
    gsap.to(el, {
        duration: 0.2,
        delay: 0.5,
        opacity: 0,
        onComplete: done
    })
}
</script>

<template>
    <nav class="p-6 relative z-20 h-16 md:py-300 md:px-1000">
        <div class="w-81.75 flex justify-between md:w-152 ">
            <img :src="logoDark" alt="Logo">

            <img :src="openMenu ? iconClose : hamburger" alt="menu-icon" class="lg:hidden"
                @click="openMenu = !openMenu">
        </div>

        <Transition @before-enter="onBeforeEnter" @enter="onEnter" @leave="onLeave" :css="false">
            <div @click.stop="openMenu = false"
                class="h-screen absolute z-10 left-0 top-0 w-full overflow-auto bg-linear-0 to-black/50 flex"
                v-if="openMenu">
                <div class="bg-white h-fit w-full mt-10 mx-4 flex flex-col text-center gap-5 p-5 rounded">
                    <a href="#">Home</a>
                    <a href="#">About</a>
                    <a href="#">Contact</a>
                    <a href="#">Blog</a>
                    <a href="#">Careers</a>
                </div>
            </div>
        </Transition>
        <div class="hidden lg:block list-none">
            <ul class="flex gap-3">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">Careers</a></li>
            </ul>
        </div>

        <div class="hidden lg:block">
            <button class="rounded-full bg-linear-to-tr from-Cyan to-75% to-Green font-semibold text-white p-3">Request
                Invite</button>
        </div>
    </nav>
</template>