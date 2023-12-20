<script setup lang="ts">
import { onMounted, ref } from 'vue'
import projectData from '@/assets/projects/data.json'
import Masonry from 'masonry-layout'

const projects = projectData.projects
let msnryEl = ref(null)
let msnry = ref({})

onMounted(() => {
    msnry.value = new Masonry('.cards', {
        itemSelector: '.card-panel',
        gutter: 30
    })
})
</script>

<template>
    <div class="projects" data-aos="fade-down" data-aos-duration="500">
        <div class="container">
            <h2 data-aos="fade-right">Projects <small class="bbn">ᜉ᜔ᜍᜓ︀ᜌᜒ︀ᜃ᜔ᜆᜓ︀</small></h2>

            <div class="cards" ref="msnryEl">
                <div class="card-panel waves-effect" :key="i" v-for="(p, i) in projects">
                    <h3>{{ p.title }}</h3>
                    <p>
                        {{ p.desc }}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.projects {
    padding: 2rem 0 10rem 0;
    background-color: var(--primary-color);

    h2 {
        margin-top: unset;
        margin-bottom: 3rem;
        font-weight: 500;
        font-size: 2.5rem;
        color: #fff;
    }

    .cards {
        .card-panel {
            margin: unset;
            margin-bottom: 2rem;
            overflow: hidden;
            box-shadow: unset;
            background-size: 100% 200%;
            background-position: 0 0;
            background-image: linear-gradient(
                to bottom,
                #fff 0%,
                #fff 25%,
                var(--primary-color-lighten-45) 50%,
                var(--primary-color-lighten-35) 100%
            );
            transition: background-position 0.3s ease;
            width: 30%;

            @media #{$m-d} {
                width: calc(50% - 2rem);
            }

            @media #{$s-d} {
                width: 100%;
            }

            &:hover {
                background-position: 100% 100%;
            }

            h3 {
                margin-top: unset;
                font-weight: 700;
                font-size: 1.5rem;
            }
        }
    }
}
</style>
