<script setup>
import Navigation from '@components/Navigation.vue';
import SideArticles from '@components/SideArticles.vue';


import SmallImage1 from "@/assets/images/image-retro-pcs.jpg";
import SmallImage2 from "@/assets/images/image-top-laptops.jpg";
import SmallImage3 from "@/assets/images/image-gaming-growth.jpg";
import HeroImage from "@/assets/images/image-web-3-desktop.jpg";
import HeroImageMobile from "@/assets/images/image-web-3-mobile.jpg";

</script>

<template>
    <Navigation />

    <div class="main-article-wrapper">
        <article class="main-article">
            <img class="main-article__hero-image" :src="HeroImage" alt="">
            <img class="main-article__hero-image mobile" :src="HeroImageMobile" alt="">
            <div class="article-small__content">
                <h1>
                    The Bright Future of Web 3.0?
                </h1>
                <div class="article-small__text">
                    <p>
                        We dive into the next evolution of the web that claims to put the power of the platforms back into
                        the hands of the people. But is it really fulfilling its promise?
                    </p>
                    <a href="#" class="button">
                        READ MORE
                    </a>
                </div>
            </div>
        </article>

        <SideArticles />
    </div>

    <div class="mini-articles">
        <article class="article-small">
            <a href="#">
                <img :src="SmallImage1" alt="">
                <div class="article-small__content">
                    <small>01</small>
                    <h4>
                        Reviving Retro PCs
                    </h4>
                    <p>
                        What happens when old PCs are given modern upgrades?
                    </p>
                </div>
            </a>
        </article>
        <article class="article-small">
            <a href="#">
                <img :src="SmallImage2" alt="">
                <div class="article-small__content">
                    <small>02</small>
                    <h4>
                        Top 10 Laptops of 2022
                    </h4>
                    <p>
                        Our best picks for various needs and budgets.
                    </p>
                </div>
            </a>
        </article>
        <article class="article-small">
            <a href="#">
                <img :src="SmallImage3" alt="">
                <div class="article-small__content">
                    <small>03</small>
                    <h4>
                        The Growth of Gaming
                    </h4>
                    <p>
                        How the pandemic has sparked fresh opportunities.
                    </p>
                </div>
            </a>
        </article>
    </div>
</template>