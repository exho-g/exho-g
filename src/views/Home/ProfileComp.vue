<template>
    <div class="profile container">
        <div class="photo" data-aos="zoom-out" data-aos-duration="1000">
            <img
                src="https://avatars.githubusercontent.com/u/32479267?v=4"
                alt="Echo"
                :key="i"
                v-for="i in 2"
            />
        </div>
        <div class="details" data-aos="fade-right" data-aos-duration="1000">
            <h1>
                Hi there! <small class="bbn">ᜋᜊᜓᜑᜌ᜔</small>
                <span>I'm Echo <small class="bbn">(ᜁᜃᜓ︀)</small></span>
            </h1>
            <div class="sns">
                <a
                    href="https://ph.linkedin.com/in/jerichog"
                    class="btn-soft waves-effect rounded"
                    title="LinkedIn"
                >
                    <i class="material-symbols-rounded left">mail</i>
                    Message me
                </a>

                <a
                    href="https://github.com/exho-g"
                    class="btn-soft waves-effect rounded danger"
                    title="Github"
                >
                    <i class="material-symbols-rounded">code</i>
                </a>
            </div>
        </div>
    </div>

    <div class="statement" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="500">
        <div class="container">
            <p>
                It's amazing how you found my page!<br />
                Whether it's because you want to try my modified version of
                <a href="https://exho-g.github.io/materialize">MaterializeCSS</a> <br />
                or you just got here from a referral link from an alternative universe,<br />
                still, thank you for visiting! 💖
            </p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.profile {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 3rem;

    @media #{$s-d} {
        flex-direction: column;
    }

    .photo {
        position: relative;
        width: 256px;
        height: 256px;

        img {
            height: 100%;
            width: 100%;
            border-radius: 50%;
            z-index: 1;

            &:nth-child(1) {
                position: absolute;
                left: 0;
                top: 2rem;
                filter: blur(36px);
                opacity: 0.7;

                @media #{$s-d} {
                    top: 1rem;
                    opacity: 0.7;
                }
            }
        }
    }

    .details {
        @media #{$s-d} {
            text-align: center;
        }
        h1 {
            font-weight: 600;
            margin-top: unset;
            margin-bottom: 1rem;
            font-size: 1.5rem;
            line-height: 1;

            span {
                font-size: 3rem;
                display: block;
            }
        }

        .sns {
            display: flex;
            gap: 0.25rem;

            @media #{$s-d} {
                justify-content: center;
            }

            a {
                margin: unset;
                i.left {
                    margin-right: 8px;
                }
            }
        }
    }
}

.statement {
    margin-top: 4rem;
    padding-bottom: 4rem;
    background-image: linear-gradient(to bottom, rgba(#000, 0), rgba(#000, 0.1));

    @media #{$s-d} {
        margin-top: 2rem;
    }

    .container {
        padding: 2rem 0;

        p {
            text-align: center;
            font-size: 1.2rem;
            position: relative;

            &::after {
                content: '';
                position: absolute;
                left: 50%;
                transform: translateX(-50%);
                bottom: -1.5rem;
                height: 6px;
                width: 20%;
                border-radius: 3px;
                background-color: hsla(var(--primary-color-hsl), 0.5);
            }
        }
    }
}
</style>
