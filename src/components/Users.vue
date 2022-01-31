<template>
  <div class="users-wrapper">
    <form @submit.prevent="submit">
      <ul>
        <li v-for="value in stock" :key="value.stock">
          <button type="submit">Выбрать</button>
          <img class="avatar-img" :src="value.avatar_url" alt="img" />
          <span>Login: {{ value.login }}</span>
        </li>
      </ul>
    </form>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Users",
  components: {},
  data() {
    return {
      stock: [],
      errors: [],
      count: 0,
    };
  },
  created() {
    axios
      .get("https://api.github.com/users")
      .then((responce) => {
        this.stock = responce.data;
        console.log(responce.data);
      })
      .catch((e) => {
        this.errors.push(e);
      });
  },
  methods: {},
};
</script>

<style scoped>
.users-wrapper {
  width: 100%;
}
.avatar-img {
  width: 60px;
  height: 60px;
  margin: 0 20px;
}
ul {
  margin-left: 100px;
}
span {
  font-size: 20px;
}
li {
  cursor: pointer;
  margin: 5px 0;
  list-style: none;
  padding: 10px;
  border: 1px solid #222;
  display: flex;
  align-items: center;
}
button {
  padding: 10px;
  background: #222;
  color: #fff;
  font-size: 16px;
  border: none;
}
button:hover {
  padding: 10px;
  background: tomato;
  color: #fff;
  font-size: 16px;
}
</style>