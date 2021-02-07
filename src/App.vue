<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-toolbar-title>Smart Catheter</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text href="https://arxiv.org/abs/2102.01932">
        <span>Paper</span>
        <v-icon right>mdi-file</v-icon>
      </v-btn>
      <v-btn text href="https://github.com/termlab/smart-catheter">
        <span>Code</span>
        <v-icon right>mdi-code-braces</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-row>
          <v-col cols=12 class="text-center">
            <h1>Smart Catheter</h1>
            <p>description of dataset</p>
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
    //
  }),
};
</script>
