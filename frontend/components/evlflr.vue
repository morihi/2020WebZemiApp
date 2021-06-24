<template>
  <v-card :loading="loading" class="mx-auto my-12" max-width="374">
    <v-card-title>■ 6F ▼</v-card-title>
    <v-card-actions>
      <v-btn @click="reserve"> 評価投稿 </v-btn>
    </v-card-actions>

    <v-card-text>
      <div class="ml-1 mt-3">現在の混雑度：　やや混んでいます</div>
      <v-row class="ml-1 mt-3">
        <span>総合評価： </span>
        <v-rating
          :value="4.0"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="ml-4">4.0 <a href="#">クチコミ(43)</a></div>
      </v-row>

      <v-divider class="ml-1 mt-6"></v-divider>

      <div class="ml-1 mt-6">混雑する時間帯：　</div>
      <img src="crowd_graph.png" alt="icon" title="icon">
      <div class="ml-1 mt-3">口コミの概要：　</div>
      <img src="review_graph.png" alt="icon" title="icon">
      <div style="display: block; margin: 2%;">
        <img src="image.png" alt="icon" title="icon" style="display: inline-block; width: 10%; height: 10%; object-fit: cover; margin-right: 1%;">
        <div style="display: inline-block;">
          <v-row class="ml-1 mt-0">
          <span>トイレットペーパーがちぎりにくい</span><br>
          </v-row>
          <v-row class="ml-1 mt-3">
            <v-rating :value="3.0" color="amber" dense half-increments readonly size="14"></v-rating>
            <div class="ml-4"><a href="">good</a>:3　<a href="">bad</a>:0</div>
          </v-row>
          </span>
        </div>
      </div>
      <div style="display: block; margin: 2%;">
        <img src="image.png" alt="icon" title="icon" style="display: inline-block; width: 10%; height: 10%; object-fit: cover; margin-right: 1%;">
        <div style="display: inline-block;">
          <v-row class="ml-1 mt-0">
          <span>割と広くて使いやすい。</span><br>
          </v-row>
          <v-row class="ml-1 mt-3">
            <v-rating :value="5.0" color="amber" dense half-increments readonly size="14"></v-rating>
            <div class="ml-4"><a href="">good</a>:4　<a href="">bad</a>:1</div>
          </v-row>
          </span>
        </div>
      </div>
      <div style="display: block; margin: 2%;">
        <img src="image.png" alt="icon" title="icon" style="display: inline-block; width: 10%; height: 10%; object-fit: cover; margin-right: 1%;">
        <div style="display: inline-block;">
          <v-row class="ml-1 mt-0">
          <span>かなり綺麗だった！！</span><br>
          </v-row>
          <v-row class="ml-1 mt-3">
            <v-rating :value="5.0" color="amber" dense half-increments readonly size="14"></v-rating>
            <div class="ml-4"><a href="">good</a>:0　<a href="">bad</a>:0</div>
          </v-row>
          </span>
        </div>
      </div>
    </v-card-text>
  </v-card>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import Review from '~/components/review.vue'
import Overview from '~/components/evlov.vue'
import Floor from '~/components/evlflr.vue'

export default {
  components: {
    Logo,
    VuetifyLogo,
    Review,
    Overview,
    Floor,
  },
}
</script>



