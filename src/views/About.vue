<template>
  <div class="about">
    <h1>This is an about page</h1><br>
      <v-btn><v-avatar size="40">
        <v-img :src="this.$store.state.fireUser.photoURL"></v-img>
      </v-avatar></v-btn>
      <h2>name : {{ name }}</h2>
      <h2>email : {{ email }}</h2>
      <h2>uid : {{ uid }}</h2>
    <site-sign></site-sign>
  </div>
</template>
<script>
import SiteSign from '@/views/site/sign'
export default {
  components: {
    SiteSign
  },
  data () {
    return {
      name: this.$store.state.fireUser.displayName,
      email: this.$store.state.fireUser.email,
      photoUrl: this.$store.state.fireUser.photoUrl,
      emailVerified: this.$store.state.fireUser.emailVerified,
      uid: this.$store.state.fireUser.uid
    }
  }
}
</script>
