<template>
  <v-card :loading="loading" class="mx-auto my-12" max-width="374">
    <v-card-title>{{ name }}</v-card-title>

    <v-card-text>
      <div class="ml-1">所在地： {{ address }}</div>
      <v-row class="ml-1 mt-3">
        <span>総合評価: </span>
        <v-rating
          :value=rate
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="ml-4">{{rate.toFixed(1)}} <a href="#">クチコミ({{ numOfReviews }})</a></div>
      </v-row>

      <div class="ml-1 mt-6">時間：　{{ openTime }} - {{ closeTime }}</div>

      <div class="ml-1 mt-2">
        投稿報酬：　お店クーポンなど<a href="#">{{ numOfCoupons }}件</a>
      </div>

      <v-row class="ml-1 mt-9" align-content="center">
        <p>お気に入りに追加する</p>
        <v-btn icon color="pink"><v-icon>mdi-heart</v-icon></v-btn>
      </v-row>
    </v-card-text>

    <div
      v-for="(item, i) in floor"
      :key="i"
    >
    <v-card-title>■ {{ item.floor }}F ▼</v-card-title>

    <v-card-text>
      <div>
        <p>現在の混雑度：</p>
        <v-rating
          v-model="item.crowd"
          length="5"
          full-icon="mdi-square"
          half-icon="mdi-square"
          empty-icon="mdi-square-outline"
        >
        </v-rating>
      </div>

      <div class="mt-4">
        <p>このトイレを評価する：</p>
        <v-rating
          v-model="item.rating"
          length="5"
        > </v-rating>
      </div>
      <div class="mt-4">
        <p>クチコミを投稿する（任意）：</p>
        <v-textarea v-model="item.review" solo></v-textarea>
      </div>
    </v-card-text>

    </div>

    <v-card-actions>
      <v-btn @click="postForm"> 投稿 </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  /**
   * UIにバインドするための変数
   */
  data() {
    return {
      /** 施設名 */
      name: 'グランパーク田町',
      /** 施設のレビュー評価 */
      rate: 4,
      /** 施設の住所 */
      address: '東京都港区芝浦1丁目',
      /** レビュー数 */
      numOfReviews: 413,
      /** 開店時間 */
      openTime: '8:00',
      /** 閉店時間 */
      closeTime: '22:00',
      /** 利用可能クーポン数 */
      numOfCoupons: 214,
      /** 投稿する画面情報 */
      floor: [
        {
          floor: 6,
          crowd: null,
          rating: null,
          review: ''
        },
        {
          floor: 7,
          crowd: null,
          rating: null,
          review: ''
        }
        ],
    }
  },
  methods: {
    postForm() {
      alert(`${this.floor[0].floor}Fの混雑度は ${this.floor[0].crowd}です。\n ${this.floor[0].floor}Fの評価は ${this.floor[0].rating}です \n ${this.floor[0].floor}Fのクチコミは ${this.floor[0].review}です`);
    }
  }
}
</script>
