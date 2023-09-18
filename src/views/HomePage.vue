<script setup lang="ts">
import Profile from './Home/ProfileComp.vue'
import Materialize from './Home/MaterializeComp.vue'
import Projects from './Home/ProjectsComp.vue'
</script>

<template>
    <main>
        <Profile />
        <Materialize />
        <Projects />
    </main>
</template>

<style lang="scss" scoped>
main {
    overflow: hidden;
    padding-top: 10rem;
}
</style>
