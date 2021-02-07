<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-img
        :src="require('./assets/logo/CLEAN.png')"
        max-height="64px"
        max-width="64px"
        contain
      ></v-img>
      <v-toolbar-title class="ml-2">
        Smart CFE Catheter Project
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-menu left bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            v-bind="attrs"
            v-on="on"
            icon
          >
            <v-icon>mdi-translate</v-icon>
          </v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="idx in availableLanguages"
            :key="idx"
            @click="changeLanguage(idx)"
          >
            <v-list-item-title>{{ languages[idx] }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-row>
          <v-col cols=12 class="text-center">
            <h1>Smart Contact Force Estimating Catheter</h1>
            <p>description of dataset</p>
            <v-btn href="https://arxiv.org/abs/2102.01932" class="mr-3">
              <span>Paper</span>
              <v-icon right>mdi-file</v-icon>
            </v-btn>
            <v-btn href="https://github.com/termlab/smart-catheter">
              <span>Code</span>
              <v-icon right>mdi-code-braces</v-icon>
            </v-btn>
          </v-col>
          <v-col cols=12>
            <h2>How did we collected?</h2>
            <p>description</p>
          </v-col>
          <v-col cols=12>
            <h2>Validation</h2>
            <p>description</p>
          </v-col>
          <v-col cols=12>
            <h2>Download</h2>
            <p>description</p>
            <v-row>
              <v-btn class="mx-3">
                <span>Train data</span>
                <v-icon right>mdi-download</v-icon>
              </v-btn>
              <v-btn>
                <span>Test data</span>
                <v-icon right>mdi-download</v-icon>
              </v-btn>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  metaInfo: {
    title: 'Smart Catheter',
    titleTemplate: '%s'
  },
  data: () => ({
    languages: ['English', '한국어', '中文', '日本語'],
    currentLanguage: 0,
    height: '128px'
  }),
  computed: {
    availableLanguages: function() {
      let result = [];
      for (let idx in this.languages) {
        if (idx != this.currentLanguage) {
          result.push(idx);
        }
      }

      return result;
    }
  },
  methods: {
    changeLanguage: function(idx) {
      this.currentLanguage = idx;
    }
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Crimson+Text&display=swap');

.v-application {
  font-family: 'Crimson Text', sans-serif !important;
}
</style>
