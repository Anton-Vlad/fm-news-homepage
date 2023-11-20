<script setup>
import logoIcon from "@/assets/images/logo.svg";
import mobileNavIcon from "@/assets/images/icon-menu.svg";
import mobileNavCloseIcon from "@/assets/images/icon-menu-close.svg";
import { ref } from "vue";

const openNav = ref(false);
const showNav = ref(false);

const openSideNav = function () {
    openNav.value = true;

    setTimeout(() => {
        showNav.value = true;
    }, 30)
}

const closeSideNav = function () {
    showNav.value = false;

    setTimeout(() => {
        openNav.value = false;
    }, 200)
}

</script>
<template>
    <nav>
        <div class="nav-logo">
            <img :src="logoIcon" alt="logo">
        </div>
        <div>
            <img v-if="!openNav" class="nav-logo-mobile" :src="mobileNavIcon" alt="menu" @click="openSideNav">
            <img v-if="openNav" class="nav-logo-mobile" :src="mobileNavCloseIcon" alt="menu" @click="closeSideNav">
        </div>
        <ul :class="`nav-menu ${showNav ? 'nav-menu--visible' : ''}`">
            <li>
                <a hre="#">Home</a>
            </li>
            <li>
                <a hre="#">New</a>
            </li>
            <li>
                <a hre="#">Popular</a>
            </li>
            <li>
                <a hre="#">Trending</a>
            </li>
            <li>
                <a hre="#">Categories</a>
            </li>
        </ul>
    </nav>

    <div :class="`opacity-layer ${showNav ? 'opacity-layer--visible' : ''} ${openNav ? 'opacity-layer--active' : ''}`"
        @click="closeSideNav">
    </div>
</template>