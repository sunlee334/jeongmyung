<template>
  <NuxtLayout>
    <v-app>

      <!-- app-bar start -->
      <v-app-bar :elevation="2">
        <v-img max-width="150" src="/img/logo.png" class=""></v-img>
        <!-- <v-app-bar-title>정명</v-app-bar-title> -->

        <template v-slot:append>
          <v-btn to="/" variant="text" class="mx-sm-1"><b>홈</b></v-btn>
          <v-btn to="/equipment" variant="text" class="mx-sm-1"><b>분석장비 및 측정항목</b></v-btn>
          <v-btn to="/info" variant="text" class="mx-sm-1"><b>측정안내</b></v-btn>
          <v-btn href="https://docs.google.com/forms/d/1YDLoqGXba3wm3-B1qWLsL3YeLUJxKdVFC_k_m9yC65w" target="_blank" variant="flat" class="mx-sm-1"rounded color="green-darken-4" size="large">
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
