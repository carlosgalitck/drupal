<template>
    <div class="header-container">
        <div class="logo-container">
            <NuxtLogo />
            <h1>TCK Nuxt</h1>
        </div>
        <div class="menu-container">
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/prueba/about">About</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyHeader',
}
</script>
 
<style>
@import '~/assets/css/header.css';
</style>