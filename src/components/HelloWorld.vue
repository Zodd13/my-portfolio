<template>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" />
  <div class="main--container">
    <div id="hello" class="main--container__title">
      <h1>HELLO</h1>
    </div>
    <div class="main--container__presentation">
      <p>
        Hello, my name is Mounir and I am a junior web developer who has just finished his training.
        <br>
        <br>
        I wish to continue my learning with a training in company, to perfect my competences and to gain in experiences.
        <br>
        <br>

        You will find on my portfolio, the projects I have done, how to contact me and my resume.
      </p>
    </div>
    <div className="main--container__arrow">
      <a href="#mywork"><i class="fa-solid fa-chevron-down"></i></a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style lang="scss">
a {
  text-decoration: none;
}

.main--container {
  height: 100vh;
  background-color: #d6ccc2;

  &__title {
    h1 {
      display: flex;
      margin-left: 2rem;
      color: white;
      margin-top: 0;
      font-family: "Montserrat", sans-serif;
      font-size: 10rem;
    }
  }

  &__presentation {
    p {
      display: flex;
      width: 50%;
      text-align: justify;
      margin: auto;
      font-size: 1.4rem;

    }
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
}
</style>
