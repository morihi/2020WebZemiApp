<template>
  <!--<review></review>-->
  <!--<briefinfo></briefinfo>-->
  <!--<briefinfolist></briefinfolist>-->
  <!--<overview></overview>-->
  <!--<floor></floor>-->
  <div>
    <div style="display: block; width: 100%; height: 15%;">
      <v-card :loading=false class="mx-auto my-12" style="background: black;">
        <v-card-title>トイレ検索アプリ</v-card-title>
      </v-card>
    </div>

    <div style="display: block; width: 100%; height: 85%; font-size: 0; background: black;">
      <div style="display: inline-block; width: 25%; height: 100%; font-size: 0; background: black;">
        <briefinfo></briefinfo>
        <briefinfo></briefinfo>
        <briefinfo></briefinfo>
        <briefinfo></briefinfo>
        <briefinfo></briefinfo>
        <briefinfo></briefinfo>
        <briefinfo></briefinfo>
      </div>
      <div style="display: inline-block; font-size: 14px; width: 25%; height: 100%; background: black; vertical-align: top;">
        <overview></overview>
        <floor></floor>
        <floor></floor>
      </div>
      <div style="display: inline-block; font-size: 12px; width: 50%; height: 100%; vertical-align: top;">
        <img src="map.png" alt="map" title="map">
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import Review from '~/components/review.vue'
import BriefInfoList from '~/components/briefinfo_list.vue'
import Overview from '~/components/evlov.vue'
import Floor from '~/components/evlflr.vue'

export default {
  components: {
    Logo,
    VuetifyLogo,
    Review,
    BriefInfoList,
    Overview,
    Floor,
  },
}
</script>
