<template>
  <div>
    <b-sidebar position="fixed" :fullheight="true" type="is-white" open>
      <aside class="u-padding">
        <div class="u-margin-left-small  block">
          <nuxt-link :to="localePath('/')">
            <logo />
          </nuxt-link>
        </div>

        <b-menu class="has-text-weight-medium">
          <b-menu-list>
            <b-menu-item
              icon="text-box-multiple-outline"
              :label="$t('pages.hymns.title')"
              tag="nuxt-link"
              :to="localePath('/hymns')"
            ></b-menu-item>

            <b-menu-item
              icon="book-multiple-outline"
              :label="$t('pages.hymnals.title')"
              tag="nuxt-link"
              :to="localePath('/hymnals')"
            ></b-menu-item>
          </b-menu-list>
        </b-menu>
      </aside>
    </b-sidebar>

    <main role="main" class="c-main-content">
      <b-navbar :fixed-top="true" :shadow="true" :spaced="true"></b-navbar>

      <nuxt />
    </main>
  </div>
</template>

<script>
import Logo from '~/components/Logo'

export default {
  components: {
    Logo
  },

  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        }
      ]
    }
  }
}
</script>

<style scoped>
.c-main-content {
  margin-left: 280px;
}
</style>
