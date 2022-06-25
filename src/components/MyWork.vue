<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" />
    <div class="main--container">
        <div id="mywork" class="main--container__title">
            <h1>MY WORK</h1>
        </div>
        <div class="main--container__cards">
            <div class="main--container__card">

                <div class="grid-item">
                    <a href="https://zodd13.github.io/P2-Reservia/P2_bernia_code/index.html" target="_blank"
                        class="grid-item__link">Visitez le site</a>
                    <img src="../assets/reservia.png" alt="Image du projet Reservia">
                </div>

                <div class="grid-item">
                    <a class="grid-item__link" href="https://zodd13.github.io/P3-Ohmyfood/" target="_blank">Visitez le
                        site</a>
                    <img src="../assets/ohmyfood.png" alt="Image du projet Oh My Food">
                </div>

                <div class="grid-item">
                    <a class="grid-item__link" href="https://zodd13.github.io/P4-Chouette/index.html"
                        target="_blank">Visitez le
                        site</a>
                    <img src="../assets/chouette.png" alt="Image du projet La chouette agence">
                </div>

                <div class="grid-item">
                    <a class="grid-item__link" href="https://github.com/Zodd13/P5-Kanap" target="_blank">Voir le repo
                        github</a>
                    <img src="../assets/kanap.png" alt="Image du projet KANAP">
                </div>

                <div class="grid-item">
                    <a class="grid-item__link" href="https://github.com/Zodd13/P7-Groupomania" target="_blank">Voir le
                        repo github</a>
                    <img src="../assets/icon.svg" alt="Image du projet Groupomania">
                </div>

            </div>
        </div>

        <div className="main--container__arrow">
            <a href="#skills"><i class="fa-solid fa-chevron-down"></i></a>
        </div>
    </div>
</template>

<script>

export default {
    name: 'MyWork'
}
</script>

<style scoped lang="scss">
.main--container {
    &__title {
        h1 {
            display: flex;
            justify-content: flex-end;
            margin-right: 2rem;
            margin-bottom: 3rem;
        }
    }

    &__cards {
        display: flex;
        width: 80%;
        margin: auto;

    }

    &__card {
        display: grid;
        grid-gap: 1rem;
        width: 100%;
        grid-template-columns: repeat(5, 1fr);

    }
    &__arrow {
        display: flex;
        height: 10%;
        width: 100%;
        align-items: flex-end;
        justify-content: center;

        .fa-chevron-down {
            color: white;
            display: flex;
            font-size: 3rem;
            height: 50px;

            &:hover {
                transform: translateY(100%);
                transition: 0.4s ease-in-out;
                cursor: pointer;
            }
        }
    }

    .grid-item {
        position: relative;
        cursor: pointer;
        background: rgba(39, 37, 32, 0.271);
        border-radius: 1rem;
        box-shadow: 1px 4px 4px 0px #00000024;

        img {
            border-radius: 1rem;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        &__link {
            position: absolute;
            margin-left: auto;
            margin-right: auto;
            left: 0;
            right: 0;
            top: 50%;
            text-decoration: none;
            color: white;
            font-weight: bold;
            font-size: 1.4rem;
            text-align: center;
            opacity: 0;

        }

        a:hover {
            color: rgba(0, 0, 0, 0.715);
        }

        &:hover {
            img {
                opacity: 0;
                z-index: -1;
                transition: all 0.5s ease-out;
            }

            a {
                opacity: 1;
                cursor: pointer;
                z-index: 2;
            }
        }
    }
}
</style>