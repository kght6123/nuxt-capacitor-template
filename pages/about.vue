<template>
  <ion-app>
    <ion-header>
      <ion-toolbar color="primary">
        <ion-title>
          Vue Capacitor | About
        </ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content padding>
      This is the About page.
      <!--nuxt-link to="/">トップへ戻る</nuxt-link-->
      <ion-button @click="goBackHome()" full>Go Back!</ion-button>
    </ion-content>
  </ion-app>
</template>

<script>
export default {
  name: 'About',
  methods: {
    goBackHome() {
      this.$router.push('/')
    }
  }
}
</script>