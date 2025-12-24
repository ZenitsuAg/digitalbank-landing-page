<script setup>
import ArticleCard from './components/ArticleCard.vue';
import Nav from './components/Nav.vue';
import WhyUs from './components/WhyUs.vue';
import logoDark from '../images/logo-dark.svg'
import logoLight from '../images/logo-light.svg'
import imageMockups from '../images/image-mockups.png'
import iconOnlineBanking from '../images/icon-online.svg'
import iconBudgeting from '../images/icon-budgeting.svg'
import iconOnboarding from '../images/icon-onboarding.svg'
import iconApi from '../images/icon-api.svg'
import imageCurrency from '../images/image-currency.jpg'
import imageRestaurant from '../images/image-restaurant.jpg'
import imagePlane from '../images/image-plane.jpg'
import imageConfetti from '../images/image-confetti.jpg'
import iconFacebook from '../images/icon-facebook.svg'
import iconYoutube from '../images/icon-youtube.svg'
import iconTwitter from '../images/icon-twitter.svg'
import iconPinterest from '../images/icon-pinterest.svg'
import iconInstagram from '../images/icon-instagram.svg'



</script>

<template>
    <Nav />

    <main class="font-public-sans bg-gray-50">

        <section class="relative">
            <div
                class="bg-[url(../images/bg-intro-mobile.svg)] md:bg-[url(../images/bg-intro-desktop.svg)] bg-right bg-no-repeat h-69.75 overflow-hidden relative">

                <img :src="imageMockups" alt="bgIntro" class="absolute -top-33.25 left-0">

            </div>

            <div class="mx-6 text-center mt-12 mb-14">
                <h1 class="font-light text-[40px] leading-[120%] tracking-[-0.75px] text-Blue">Next generation digital
                    banking
                </h1>

                <p class="font-normal text-sm my-6 text-gray-600">
                    Take your financial life online. Your Digitalbank account will be a one-stop-shop
                    for spending, saving, budgeting, investing, and much more.
                </p>

                <button class="py-2 px-8 font-bold text-white text-sm leading-[200%] rounded-[22px] gradient-1 ">Request
                    Invite</button>
            </div>
        </section>

        <section class="bg-gray-100 py-16 px-6 text-center">
            <div class="">
                <h1 class="text-preset-3"> Why choose Digitalbank?</h1>

                <p class="text-preset-7 text-gray-600 mt-4 mb-12">We leverage Open Banking to turn your bank account
                    into your financial hub. Control your finances like never before.</p>

                <div class="flex flex-col gap-8">
                    <WhyUs :img-src="iconOnlineBanking" img-alt="iconOnlineBanking" title="Online Banking"
                        content="Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world." />

                    <WhyUs :img-src="iconBudgeting" img-alt="iconBudgeting" title="Simple Budgeting"
                        content=" See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits." />

                    <WhyUs :img-src="iconOnboarding" img-alt="iconOnboarding" title="Fast Onboarding"
                        content="We don’t do branches. Open your account in minutes online and start taking control of your finances right away." />

                    <WhyUs :img-src="iconApi" img-alt="iconApi" title="Open API"
                        content=" Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier." />

                </div>
            </div>
        </section>

        <section>
            <div class="my-800 px-300">
                <h1 class="text-preset-3 text-center text-Blue mb-600">Latest Articles</h1>
                <div class="flex flex-col gap-200">
                    <ArticleCard :img="imageCurrency" alt="image-currency" by="Claire Robinson"
                        title="Receive money in any currency with no fees"
                        details="The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single …" />

                    <ArticleCard :img="imageRestaurant" alt="image-restaurant" by="Wilson Hutton"
                        title="Treat yourself without worrying about money"
                        details="Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …" />

                    <ArticleCard :img="imagePlane" alt="image-plane" by="Wilson Hutton"
                        title="Take your Digitalbank card wherever you go"
                        details="We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …" />

                    <ArticleCard :img="imageConfetti" alt="image-confetti" by="Claire Robinson"
                        title="Our invite-only Beta accounts are now live!"
                        details="After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site ..." />
                </div>
            </div>

        </section>


        <footer class="h-127.5 py-700 bg-Blue text-white">
            <div class="flex flex-col items-center">
                <img :src="logoLight" alt="logo">

                <div id="social" class="flex gap-200 my-400">
                    <img :src="iconFacebook" alt="icon-facebook">
                    <img :src="iconYoutube" alt="icon-youtube">
                    <img :src="iconTwitter" alt="icon-twitter">
                    <img :src="iconPinterest" alt="icon-pinterest">
                    <img :src="iconInstagram" alt="icon-instagram">
                </div>

                <ul class="flex flex-col gap-200 mb-400 text-preset-7">
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Contact</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Careers</a></li>
                    <li><a href="#">Support</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                </ul>

                <button class="gradient-1 text-preset-7-bold py-100 px-400 rounded-[22px]">Request Invite</button>

                <p class="mt-300 text-preset-7 text-gray-600"> © Digitalbank. All Rights Reserved</p>
            </div>

        </footer>


    </main>

</template>

<style scoped></style>
