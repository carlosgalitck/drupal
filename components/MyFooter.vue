<template>
    <div class="header-container footer-container">
        <div class="logo-container">
            <NuxtLogo />
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
    name: 'MyFooter',
}
</script>
 
<style>
@import '~/assets/css/footer.css';
</style> 