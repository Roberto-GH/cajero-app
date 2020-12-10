<!-- TEMPLATE representa el html (estrucuctura)-->
<template>
  <div id="User">
    <h2>Hola <span> {{ username }}, </span> ¡Bienvenido!</h2>
  </div>
</template>

<!-- SCRIPT representa el js (comportamiento)-->
<script>
export default {
  name: "User",
  data: function () {
    return {
      username: "none",
    };
  },
  created: function () {
    this.username = this.$route.params.username;
  },
};
</script>

<!-- STYLE representa el css (estilo)-->
<style>
#User {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
#User h2 {
  font-size: 50px;
  color: #283747;
}
#User span {
  color: crimson;
  font-weight: bold;
}
</style>