<template>
  <nav>
    <div class="wrapper-naw">
      <router-link to="/">Logo</router-link>
      <ul>
        <router-link tag="li" to="/" exact-active-class="active"
          ><a href="#">Home</a></router-link
        >
        <router-link tag="li" to="/UserSelected"
          ><a href="#">UserSelected</a></router-link
        >
      </ul>
      <input class="sirch" type="text" placeholder="Sirch" />
    </div>
  </nav>
</template>

<script>
export default {
  name: "Header",
  components: {},
};
</script>

<style scoped>
nav {
  max-width: 100%;
  background: #222;
  padding: 20px 0;
}
nav a {
  font-weight: bold;
  color: #fff;
  margin: 0 20px;
  font-size: 24px;
  text-decoration: none;
}
nav a:hover {
  color: red;
  text-decoration: underline;
}
/* nav a.router-link-exact-active {
  color: #42b983;
} */
.wrapper-naw {
  max-width: 1400px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
li {
  margin: 20 px 0;
  list-style: none;
}
.sirch {
  width: 200px;
  height: 20px;
  margin-right: 26px;
}
</style>