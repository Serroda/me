<script lang="ts" setup>
import { ref } from "vue";

const isSmall = ref(window.matchMedia("(max-width: 1055px)").matches);

window.onresize = () => {
  isSmall.value = window.matchMedia("(max-width: 1055px)").matches;
};
</script>

<template>
  <div class="container">
    <section>
      <h1 class="title">
        <img class="letters" src="./assets/jota.svg" />esús
        <img class="letters" src="./assets/ce.svg" />árceles
      </h1>
      <div class="m-auto">
        <p class="animation-typing">desarrollador de aplicaciones web</p>
      </div>
      <a
        v-if="!isSmall"
        href="https://es.linkedin.com/in/jes%C3%BAs-c%C3%A1rceles-119108234"
        target="_blank"
        class="button-linkedin"
        >Linkedin</a
      >
    </section>
    <section>
      <p>Hola.</p>
      <p>
        Soy un desarrollador con experiencia en Frontend y Backend, además con
        conocimientos de SQL Server.
      </p>
      <p>
        Desarrollo con
        <a href="https://vuejs.org/" class="color-vue" target="_blank"
          >Vue.js</a
        >
        y
        <a
          href="https://learn.microsoft.com/es-es/dotnet/core/introduction"
          class="color-net"
          target="_blank"
          >.NET Core</a
        >, juntos forman un buen equipo para crear aplicaciones web,
        aplicaciones para movíles y servicios rápidos y eficientes.
      </p>
      <p>
        Tambien me gusta experimentar con
        <a href="https://www.figma.com/" class="color-figma" target="_blank"
          >Figma</a
        >
        =)
      </p>
      <a
        v-if="isSmall"
        href="https://es.linkedin.com/in/jes%C3%BAs-c%C3%A1rceles-119108234"
        target="_blank"
        class="button-linkedin"
        >Linkedin</a
      >
    </section>
  </div>
</template>
