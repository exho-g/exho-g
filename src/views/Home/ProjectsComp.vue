<template>
    <div class="projects" data-aos="fade-up">
        <div class="container">
            <h2 data-aos="fade-right">Projects <small class="bbn">ᜉ᜔ᜍᜓ︀ᜌᜒ︀ᜃ᜔ᜆᜓ︀</small></h2>

            <div class="cards staggered-cards m2 xl3">
                <div class="card-panel waves-effect" :key="i" v-for="i in 20">
                    <h3>On going project</h3>
                    <p :key="il" v-for="il in (i % 3) + 1">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint itaque
                        molestias facere iusto quos aperiam distinctio earum laboriosam dolorum
                        laudantium ducimus dolor, accusantium tempora minus in dicta eaque vel
                        aliquid?
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
