<template>
  <v-app id="inspire" dark>
    <v-navigation-drawer
    v-model="drawer"
    clipped
    fixed
    app
    >
    <v-list dense>

      <v-subheader>Generale</v-subheader>
      <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>dashboard</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Scrivania</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile @click="$router.push('impostazioni')">
        <v-list-tile-action>
          <v-icon>settings</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Impostazioni</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>

      <v-subheader>Attività</v-subheader>
      <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>calendar_today</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Calendario</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>school</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Lezioni</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>bookmark_border</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Corsi</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>

       <v-subheader>Registro</v-subheader>
       <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>recent_actors</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Studenti</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>recent_actors</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Insegnanti</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>supervisor_account</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Staff</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>

      <v-subheader>Strumenti</v-subheader>
       <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>monetization_on</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Budget</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile @click="$router.push('/')">
        <v-list-tile-action>
          <v-icon>message</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Messaggi</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </v-navigation-drawer>
  <v-toolbar app fixed clipped-left>
    <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
    <v-toolbar-title>GrimmGest</v-toolbar-title>
  </v-toolbar>
  <v-content>
    
      <router-view></router-view>
   
  </v-content>
  <v-footer app fixed>
    <span>&copy; GrimmLab 2018</span>
  </v-footer>
</v-app>
</template>

<script>

  export default {
    data: () => ({
      drawer: true,

    }),
    methods:{

    }
  }
</script>
<style lang="scss">
@import 'assets/css/main.css';
</style>