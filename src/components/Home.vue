<template>
<b-container >
  <b-row align-h="center" align-content="center" >
    <b-col style="flex-grow:unset" >
      <LocaleChanger/>
      </b-col>
  </b-row>
   <b-row align-h="center">
    <b-col>
       <p>
     {{$t('message')}}
    </p>
    </b-col>
  </b-row>
</b-container>
 
</template>

<script>
import LocaleChanger from './LocaleChanger.vue'

export default {
  name: 'Home',
  components: {
    LocaleChanger
  }
}
</script>
