<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" />
    <div class="main--container">
        <div id="skills" class="main--container__title">
            <h1>SKILLS</h1>
        </div>
        <div class="main--container">
            <div class="main--container__box">
                <div class="main--container__bar">
                    <div class="grid-item">
                        <a href="https://www.w3.org/html/" target="_blank"> <img
                                src="https://img.icons8.com/color/48/000000/html-5.png" /> </a>
                    </div>
                    <div class="main--container__external">
                        <div class="main--container__progressbarA">
                        </div>
                    </div>
                </div>

                <div class="main--container__bar">
                    <div class="grid-item">
                        <a href="https://www.w3schools.com/css/" target="_blank"> <img
                                src="https://img.icons8.com/color/48/000000/css3.png" /> </a>
                    </div>
                    <div class="main--container__external">

                        <div class="main--container__progressbarB">
                        </div>
                    </div>
                </div>

                <div class="main--container__bar">
                    <div class="grid-item">
                        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank"> <img
                                src="https://img.icons8.com/color/48/000000/javascript.png" /> </a>
                    </div>
                    <div class="main--container__external">

                        <div class="main--container__progressbarC">
                        </div>
                    </div>
                </div>

                <div class="main--container__bar">
                    <div class="grid-item">
                        <a href="https://git-scm.com/" target="_blank"> <img
                                src="https://img.icons8.com/color/48/000000/git.png" /> </a>
                    </div>
                    <div class="main--container__external">

                        <div class="main--container__progressbarD">
                        </div>
                    </div>
                </div>

                <div class="main--container__bar">
                    <div class="grid-item">
                        <a href="https://sass-lang.com" target="_blank" rel="noreferrer"> <img
                                src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sass/sass-original.svg"
                                alt="sass" width="40" height="40" /> </a>
                    </div>
                    <div class="main--container__external">

                        <div class="main--container__progressbarE">

                        </div>
                    </div>
                </div>

                <div class="main--container__bar">
                    <div class="grid-item">
                        <a href="https://vuejs.org/" target="_blank" rel="noreferrer"> <img
                                src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original-wordmark.svg"
                                alt="vuejs" width="40" height="40" /> </a>
                    </div>
                    <div class="main--container__external">

                        <div class="main--container__progressbarF">
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MySkills'
}
</script>

<style scoped lang="scss">
.main--container {
    .grid-item{
        padding: 5px;
        margin-right: 1rem;
    }

    h1 {
        margin-bottom: 3rem;
    }

    &__bar {
        display: flex;
        flex-direction: row;
        margin: auto;
        text-align: justify;
        align-items: center;
        justify-content: flex-start;
        width: 90%;
    }

    &__box {
        display: flex;
        flex-direction: column;
        box-shadow: 1px 4px 4px 0px #00000024;
        width: 50%;
        height: auto;
        padding: 1.5rem 1.5rem 1.5rem 0;
        border-radius: 1rem;
        background-color: white;
        margin: auto;
    }

    &__external {
        width: 100%;
        border-radius: 1rem;
        height: 2rem;
        background-color: #d6ccc2;
    }

    &__progressbarA,
    &__progressbarB,
    &__progressbarC,
    &__progressbarD,
    &__progressbarE,
    &__progressbarF {
        border-radius: 1rem 0rem 0rem 1rem;
        height: 2rem;
        margin: 0;
        width: 100%;
        background-color: #9e876f65;

        p {
            visibility: hidden;
        }
    }

    &__progressbarA {
        width: 75%;

        &:hover {
            p {
                visibility: visible;
                display: flex;
                margin: 0;
                height: 100%;
                justify-content: center;
                align-items: center;
            }
        }
    }

    &__progressbarB {
        width: 60%;
    }

    &__progressbarC {
        width: 65%;
    }

    &__progressbarD {
        width: 60%;
    }

    &__progressbarE {
        width: 90%;
    }

    &__progressbarF {
        width: 60%;
    }
}
</style>
