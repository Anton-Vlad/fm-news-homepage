<script setup>
import logoIcon from "@/assets/images/logo.svg";
</script>


<template>
    <nav>
        <div class="nav-logo">
            <img :src="logoIcon" alt="logo">
        </div>
        <ul class="nav-menu">
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
</template>