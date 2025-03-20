<template>
  <NuxtLayout>
    <v-app>

      <!-- app-bar start -->
      <v-app-bar :elevation="2">
        <v-img max-width="150" src="/img/logo.png" class=""></v-img>
        <!-- <v-app-bar-title>정명</v-app-bar-title> -->

        <template v-slot:append>
          <v-btn to="/" variant="text" class="mx-2" size=""><b>홈</b></v-btn>
          <v-btn to="/equipment" variant="text" class="mx-2" size=""><b>측정항목</b></v-btn>
          <v-btn to="/info" variant="text" class="mx-2" size=""><b>측정안내</b></v-btn>
          <v-btn href="https://docs.google.com/forms/d/1YDLoqGXba3wm3-B1qWLsL3YeLUJxKdVFC_k_m9yC65w" target="_blank" variant="flat" rounded color="green-darken-4" size="large">
            문의하기
          </v-btn>
        </template>
      </v-app-bar>
      <!-- app-bar end -->

      <v-main>
        <NuxtPage />
      </v-main>

    </v-app>

  </NuxtLayout>
</template>
<script>
  export default {
    computed: {
      btnSize () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return 220
          case 'sm': return 400
          case 'md': return 500
          case 'lg': return 600
          case 'xl': return 800
        }
      },
    },
  }
</script>