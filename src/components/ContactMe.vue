<script>
import useValidate from '@vuelidate/core'
import { required, email, minLength } from '@vuelidate/validators'
import { reactive, computed } from 'vue'
export default {
    setup() {
        const state = reactive({
            email: '',
            name: '',
            message: '',
        })

        const rules = computed(() => {
            return {

                email: { required, email },
                name: { required, minLength: minLength(2) },
                message: { required, minLength: minLength(5) }
            }
        })

        const v$ = useValidate(rules, state)
        return {
            state,
            v$,
        }
    },
    name: 'ContactMe',
    methods: {
        validationForm(e) {
            this.v$.$validate()
            if (!this.v$.$error) {
                alert('Le message a bien été envoyer.')
            } else {
                e.preventDefault();
                alert('Erreur dans le formulaire.')

            }
        }
    }
}
</script>

<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" />
    <div id="contact" class="main--container">
        <div class="main--container__title">
            <h1>CONTACT</h1>
        </div>
        <div class="main--container__contact">
            <form class="main--container__form" method='POST'
                action="https://getform.io/f/43a24c6e-8e1a-40fa-8259-473177bcc213">
                <div class='main--container__formtitle'>
                    <p>You can contact me by filling this form or by using my <a
                            href="mailto:berniam.pro@gmail.com">address email</a></p>
                </div>
                <input v-if="!v$.name.$error" class='main--container__nameinput' type="text" v-model="state.name"
                    placeholder='Name' name='nom' />
                <input v-else class='main--container__nameinput' type="text" v-model="state.name"
                    placeholder='Votre nom est trop court.' name='nom' />


                <input v-if="!v$.email.$error" class='main--container__emailinput' type="email" v-model="state.email"
                    placeholder='Email' name='email' />
                <input v-else class='main--container__emailinput' type="email" v-model="state.email"
                    placeholder='Votre adresse email est incorrect.' name='email' />

                <textarea resize="none" v-if="!v$.message.$error" class='main--container__text' name="message"
                    v-model="state.message" rows="10" placeholder='Message'></textarea>
                <textarea resize="none" v-else class='main--container__text' name="message" v-model="state.message"
                    rows="10" placeholder='Votre message est trop court'></textarea>
                <button name="submit" value="submit" @click="validationForm" class='main--container__button'>Send your message</button>
            </form>
        </div>
    </div>

    <div class="footer">
        <div class="footer--social">
            <a target="_blank" href="https://www.linkedin.com/in/mounirber/"><i class="fa-brands fa-linkedin"></i></a>
            <a target="_blank" href="https://github.com/Zodd13"><i class="fa-brands fa-github"></i></a>
            <a target="_blank" href="https://twitter.com/itisreda"><i class="fa-brands fa-twitter"></i></a>
        </div>
    </div>
</template>

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

    button {
        border: none;
        padding: 1rem;
        width: fit-content;
        display: flex;
        margin: auto;
        border-radius: 1rem;
        background-color: white;
        font-weight: bold;
        color: #615656d8;

        &:hover {
            cursor: pointer;
            transition: ease-in 0.6s;
            box-shadow: 1px 4px 4px 0px #00000024;
            background-color: lighten($color: #615656d8, $amount: 0);
            color: white;

        }
    }

    a {
        text-decoration: none;
        color: #615656d8;
        font-weight: bold;

        &:hover {
            color: darken($color: #615656d8, $amount: 10);
        }
    }

    input,
    textarea {
        background-color: white;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        font-weight: bold;
        resize: none;
        border: none;
        padding: 0.5rem;
        box-shadow: 1px 4px 4px 0px #00000024;
        border-bottom: 1px solid rgba(0, 0, 0, 0.261);
    }

    &__form {
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin: auto;
        width: 40%;
    }

    &__nameinput {
        border-radius: 1rem 1rem 0rem 0rem;
    }

    &__text {
        margin-bottom: 1rem;
        border-radius: 0rem 0rem 1rem 1rem;
    }
}

.footer {
    border-top: 1px solid rgba(0, 0, 0, 0.265);
    background-color: white;
    height: 5rem;
    width: 100%;
    margin: 0;

    a {
        text-decoration: none;
        color: #615656d8;
        font-weight: bold;

        &:hover {
            color: darken($color: #615656d8, $amount: 10);
        }
    }

    &--social {
        cursor: pointer;
        font-size: 2rem;
        display: flex;
        width: 20%;
        justify-content: space-evenly;
        margin: 1rem auto auto auto;
    }
}
</style>
