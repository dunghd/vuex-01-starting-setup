<template>
  <button v-if="!isAuth" @click="login">Login</button>
  <button v-if="isAuth" @click="logout">Logout</button>
</template>

<script>
import { mapActions, mapGetters } from 'vuex';

export default {
  computed: {
    ...mapGetters({ isAuth: 'userIsAuthenticated' }),
  },
  methods: {
    ...mapActions(['login', 'logout']),
  },
};
</script>
