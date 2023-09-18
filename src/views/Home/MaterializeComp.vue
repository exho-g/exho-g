<template>
    <div class="materialize" data-aos="fade-in" data-aos-duration="1000" data-aos-delay="700">
        <div
            class="circles"
            data-aos="zoom-out"
            data-aos-duration="1000"
            :key="i"
            v-for="i in 3"
        ></div>

        <div class="container">
            <div class="card-panel" data-aos="zoom-out" data-aos-duration="1000">
                <div>
                    <img
                        src="https://exho-g.github.io/materialize/res/materialize.svg"
                        alt="MaterializeCSS Modified Logo"
                    />
                    <p>If you're here for my Modified MaterializeCSS</p>
                </div>
                <a
                    href="https://exho-g.github.io/materialize"
                    class="btn-soft waves-effect large primary rounded"
                    title="Go to MaterializeCSS Documentation Page"
                >
                    Click here
                    <i class="material-symbols-rounded right">east</i>
                </a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.materialize {
    padding: 20rem 0;
    position: relative;
    background-image: linear-gradient(
        to bottom right,
        var(--primary-color-lighten-40),
        var(--secondary-color-lighten-40)
    );

    .circles {
        position: absolute;
        z-index: -0;
        border-radius: 50%;
        background-image: linear-gradient(
            to bottom right,
            var(--primary-color-lighten-45),
            var(--primary-color-lighten-20)
        );
        width: 650px;
        height: 650px;

        &:nth-child(1) {
            top: -6rem;
            left: -10%;

            @media #{$m-d} {
                left: -50%;
            }

            @media #{$s-d} {
                left: -90%;
            }
        }

        &:nth-child(2) {
            top: 26rem;
            left: 47%;
            width: 300px;
            height: 300px;

            background-image: linear-gradient(
                to bottom right,
                var(--primary-color-light),
                var(--secondary-color-lighten-20)
            );

            @media #{$m-d} {
                top: 30rem;
            }
        }

        &:nth-child(3) {
            top: 15rem;
            left: 78%;
            width: 150px;
            height: 150px;

            background-image: linear-gradient(
                to bottom right,
                var(--secondary-color-lighten-30),
                var(--secondary-color-light)
            );
        }
    }

    .container {
        .card-panel {
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: var(--floating-depth);
            background-color: rgba($color: #fff, $alpha: 0.3);
            backdrop-filter: blur(24px);
            gap: 1rem;
            border: 2px solid rgba(#fff, 0.5);

            @media #{$s-d} {
                flex-direction: column;
            }

            div {
                @media #{$s-d} {
                    text-align: center;
                }

                p {
                    margin-bottom: unset;
                    font-size: 1.2rem;
                }
            }
        }
    }
}
</style>
