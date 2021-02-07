<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-toolbar-title>Smart Catheter</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text>
        <span>Download</span>
        <v-icon right>mdi-download</v-icon>
      </v-btn>
      <v-btn text>
        <span>Paper</span>
        <v-icon right>mdi-file</v-icon>
      </v-btn>
      <v-btn text>
        <span>Code</span>
        <v-icon right>mdi-code-braces</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
