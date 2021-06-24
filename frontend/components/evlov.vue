<template>
  <v-card :loading="loading" class="mx-auto my-12" max-width="374">
    <v-card-title>グランパーク田町</v-card-title>

    <v-card-text>
      <div class="ml-1">所在地： 東京都港区芝浦1丁目</div>
      <v-row class="ml-1 mt-3">
        <span>総合評価: </span>
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="ml-4">4.5 <a href="#">クチコミ(413)</a></div>
      </v-row>

      <div class="ml-1 mt-6">時間：　8:00 - 22:00</div>

      <div class="ml-1 mt-2">
        投稿報酬：　お店クーポンなど<a href="#">3件</a>
      </div>
    </v-card-text>
  </v-card>
</template>
