<template>
  <div>
    <nav id="navbar">
      <BackButton class="navbutt" />
      <HowToPlayButton class="navbutt" />
      <LogOut class="navbutt" />
    </nav>
    <Header />
    <div id="login">
      <h1 class="error">404: Page Not Found</h1>
      <p>There are no butterflies here. Possibly due to Deforestation :(.</p>
    </div>
  </div>
</template>

<script>
import Header from "./Header.vue";
import BackButton from "./BackButton";
import HowToPlayButton from "./HowToPlayButton";
import LogOut from "./Logout";

export default {
  name: "NotFound",
  components: {
    Header,
    BackButton,
    HowToPlayButton,
    LogOut
  }
};
</script>

<style scoped>
@font-face {
  font-family: "Pacifico";
  font-style: normal;
  font-weight: 400;
  src: url("../fonts/pacifico-v16-latin-regular.eot"); /* IE9 Compat Modes */
  src: local("Pacifico Regular"), local("Pacifico-Regular"),
    url("../fonts/pacifico-v16-latin-regular.eot?#iefix")
      format("embedded-opentype"),
    /* IE6-IE8 */ url("../fonts/pacifico-v16-latin-regular.woff2")
      format("woff2"),
    /* Super Modern Browsers */ url("../fonts/pacifico-v16-latin-regular.woff")
      format("woff"),
    /* Modern Browsers */ url("../fonts/pacifico-v16-latin-regular.ttf")
      format("truetype"),
    /* Safari, Android, iOS */
      url("../fonts/pacifico-v16-latin-regular.svg#Pacifico") format("svg"); /* Legacy iOS */
}

@media screen and (min-width: 600px) {
  #login {
    width: 500pt;
    border: 4px solid #acd998;
    background-color: #e6e6fa;
    border-radius: 30px;
    margin: auto;
    padding: 20px;
    text-align: left;
    display: grid;
    margin-bottom: 2%;
    box-shadow: 0 8px 6px -6px black;
  }
  #navbar {
    margin: auto;
    display: grid;
    width: 500pt;
    grid-template-columns: 1fr 1fr 1fr;
    list-style: none;
    column-count: 3;
    column-gap: 1em;
    row-gap: 1em;
    padding: 1em;
    justify-items: center;
  }
  .navbutt {
    width: 100%;
    height: auto;
  }
}
@media screen and (max-width: 600px) {
  #login {
    width: 85%;
    border: 4px solid #acd998;
    background-color: #e6e6fa;
    border-radius: 30px;
    margin: auto;
    padding: 20px;
    text-align: left;
    display: grid;
    margin-bottom: 2%;
    box-shadow: 0 8px 6px -6px black;
  }
  #navbar {
    margin: auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    list-style: none;
    column-count: 3;
    column-gap: 1em;
    row-gap: 1em;
    padding: 1em;
  }
  .navbutt {
    width: 100%;
    height: auto;
  }
}

.error {
  color: #d95c26;
  font-size: 2em;
  margin-top: 0;
  font-family: Pacifico;
}
</style>
