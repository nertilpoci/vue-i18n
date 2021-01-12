<template>
    <b-card
     :title="$t('language')"
    :img-src="getImgUrl($i18n.locale)"
    img-alt="Image"
    img-top
    class="mb-2"
        style="max-width: 200px;"

  >
     <b-form-select     style="max-width: 200px;"
 v-model="$i18n.locale">
      <b-form-select-option v-for="(lang, i) in langs" :key="`Lang${i}`" :value="lang">{{ lang }}</b-form-select-option>
    </b-form-select>
  </b-card>
</template>

<script>
export default {
  name: 'locale-changer',
  data () {
    return { langs: ['en','de'] }
  }, 
  methods:{
    getImgUrl(pic) {
    var images = require.context('../assets/', false, /\.png$/)
    return images('./' + pic + ".png")
}
  }
}
</script>