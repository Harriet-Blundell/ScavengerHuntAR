<template>
  <router-link to="/login" v-on:click.native="this.$root.logout()">
    <button class="top-btn" v-on:click="clickHandler()">Log Out</button>
  </router-link>
</template>

<script>
import { firestore } from "firebase";
export default {
  name: "LogOut",
  methods: {
    clickHandler() {
      if (this.$route.params.username) {
        firestore()
          .doc(
            `parents/${window.localStorage.uid}/userProfiles/${this.$route.params.username}`
          )
          .update({ collectionUpdate: false });
      }
    }
  }
};
</script>

<style>
.top-link {
  text-decoration: none;
  color: white;
}

.top-btn {
  font-size: 18px;
  border-radius: 30px;

  border: 2px solid #cccccc;
  background: rgba(204, 204, 204, 0.2);
  padding: 14px 20px;
  border: none;
  border-radius: 40px;
  cursor: pointer;
  margin-top: 30px;
  margin-bottom: 10px;
}

.top-btn:hover {
  opacity: 10%;
}
</style>