<template>
  <b-container>
  <b-row align-h="center">
     
      <b-col>
        <h2>
          {{ $t("message") }}
        </h2>
      </b-col>
    </b-row>
    <b-row align-h="center">
        <b-col>
          <b-card-group deck>
         <LocaleChanger />
           <b-card
          :title="$t('pluralization')"
          class="mb-2"
          style="max-width: 300px"
        >
          <b-form-input
            type="number"
            v-model="pluralization"
          ></b-form-input>
          <b-card-text>
            <b>{{ $tc("car", pluralization, { count: pluralization }) }}</b>
          </b-card-text>
        </b-card>
          <b-card
          :title="$t('currency')"
          class="mb-2"
          style="max-width: 300px"
        >
         <b-form-input
            type="number"
            v-model="money"
          ></b-form-input>
          <b-card-text>
             <p>{{ $n(money, 'currency') }}</p>
          </b-card-text>
        </b-card>
          </b-card-group>
      </b-col>
     
      
     
    </b-row>
  </b-container>
</template>

<script>
import LocaleChanger from "./LocaleChanger.vue";

export default {
  name: "Home",
  data() {
    return {
      pluralization: 0,
      money: 10000
    };
  },
  components: {
    LocaleChanger,
  },
};
</script>
