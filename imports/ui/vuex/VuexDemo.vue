<template>
  <div class="vue-demo">
    <h1>{{ $t('pages.vuex.title') }}</h1>
    <links-menu :links="links"></links-menu>
    <router-view></router-view>
  </div>
</template>

<script>
import {store} from '/imports/vuex/store'

export default {
  store,
  data: () => ({
    links: [
      { name: 'vuex', exact: true, lb: 'pages.vuex.counter.title' },
      { name: 'vuex.tracker', lb: 'pages.vuex.tracker.title' }
    ]
  })
}
</script>
