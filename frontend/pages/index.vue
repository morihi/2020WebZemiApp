<template>
  <!--<review></review>-->
  <!--<briefinfo></briefinfo>-->
  <!--<briefinfolist></briefinfolist>-->
  <!--<overview></overview>-->
  <floor></floor>
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
