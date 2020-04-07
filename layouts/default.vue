<template>
  <div>
    <b-navbar
      type="is-primary"
      wrapper-class="container"
      :spaced="false"
      class="is-medium"
    >
      <template slot="brand">
        <b-navbar-item tag="nuxt-link" :to="localePath('/')">
          <logo class="logo" />
          <span class="is-size-4  has-text-weight-semibold">SweetHymns</span>
        </b-navbar-item>
      </template>

      <template slot="end">
        <b-navbar-item tag="router-link" :to="localePath('/')">
          {{ $t('home.title') }}
        </b-navbar-item>

        <b-navbar-item tag="router-link" :to="localePath('/hymns')">
          {{ $t('hymns.title') }}
        </b-navbar-item>

        <b-navbar-item tag="router-link" :to="localePath('/hymnals')">
          {{ $t('hymnals.title') }}
        </b-navbar-item>
      </template>
    </b-navbar>

    <main>
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
.logo {
  margin-right: 0.5rem;
}
</style>
