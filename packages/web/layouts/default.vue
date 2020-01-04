<template lang="pug">
div
  b-navbar.is-primary
    template(slot="brand")
      b-navbar-item(tag="router-link" to="/")
        strong Русский Diary
    template(slot="start")
      b-navbar-item(tag="router-link" to="/posts/alphabet") Alphabet
      b-navbar-item(tag="router-link" to="/posts/phrasebook") Phrasebook
    template(slot="end")
      b-navbar-item(tag="a" href="https://github.com/patarapolw/rudiary" target="_blank")
        b-icon(icon="github-circle")
  section.main-content.columns
    .container.column.is-10-desktop.is-offset-1-desktop
      nuxt
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component
export default class DefaultLayout extends Vue {}
</script>
