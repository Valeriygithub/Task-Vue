<template>
  <nav>
    <ul>
      <router-link tag="li" to="/" exact-active-class="active"
        ><a href="#">Пользователи</a></router-link
      >
      <router-link tag="li" to="/UserSelected"
        ><a href="#">Выбранные пользователи</a></router-link
      >
    </ul>
  </nav>
</template>

<script >
export default {
  name: "Sidebar",
};
</script>

<style scoped>
nav {
  /* max-width: 100%; */
  min-height: 520px;
  /* background: #222; */
  box-shadow: 1px 1px 8px #222;
}
nav a {
  padding: 10px 0;
  font-weight: bold;
  color: #222;
  margin: 0 12px;
  font-size: 24px;
  text-decoration: none;
}
nav a:hover {
  color: red;
  text-decoration: underline;
}
nav a.router-link-exact-active {
  color: #42b983;
}
li {
  margin: 20px 0;
}
ul {
  display: flex;
  flex-direction: column;
  align-items: start;
}
</style>