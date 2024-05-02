<template>

        <AppHeader />
        <AppMain />
        <AppBluBanner />
        <AppMainFooter />
        <AppLogoFooter />



</template>

<script>
import AppBluBanner from './components/AppBluBanner.vue'
import AppHeader from './components/AppHeader.vue'
import AppLogoFooter from './components/AppLogoFooter.vue'
import AppMain from './components/AppMain.vue'
import AppMainFooter from './components/AppMainFooter.vue'

export default {
    components: {
        AppHeader,
        AppMain,
        AppBluBanner,
        AppMainFooter,
        AppLogoFooter,
    },

}
</script>

<style></style>