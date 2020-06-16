<template>
  <div class="dashboard-container">
    <home-cilck-group @handleSetLineChartData="handleSetLineChartData" />
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

import HomeCilckGroup from './components/HomeClickGroup'

export default {
  name: 'ViewProduct',
  components: {
    HomeCilckGroup
  },
  computed: {
    ...mapGetters([
      'name'
    ])
  },
  methods: {
    handleSetLineChartData(type) {
      console.log(type)
      this.$router.push({ path: type })
    }
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
