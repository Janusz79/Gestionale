<template>
  <v-container grid-list-md fluid fill-height>
        <v-layout row wrap>
          <v-flex xs12>
            <trend
              :data="[0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0]"
              :gradient="['#6fa8dc', '#42b983', '#2c3e50']"
              auto-draw
              smooth>
            </trend>
            <svg class="over" viewBox="0 0 300 75" width="100%" height="25%">
              <rect width="1" height="300" fill="#FFFFFF" />
            </svg>
          </v-flex>
          <v-flex xs12 sm6>
              <v-card>
                <v-toolbar color="green" dark>
                  <v-toolbar-title>Messaggi</v-toolbar-title>
                </v-toolbar>
                <v-list two-line>
                  <template v-for="(item, index) in Messaggi">
                    <v-list-tile :key="index" avatar ripple @click="">
                      <v-list-tile-content>
                        <v-list-tile-title>{{ item.headline }}</v-list-tile-title>
                        <v-list-tile-sub-title class="text--primary">{{ item.from }}</v-list-tile-sub-title>
                        <v-list-tile-sub-title>{{ item.text }}</v-list-tile-sub-title>
                      </v-list-tile-content>
                      <v-list-tile-action>
                        <v-list-tile-action-text>{{ item.action }}</v-list-tile-action-text>
                        <v-icon color="grey lighten-1">star_border</v-icon>
                      </v-list-tile-action>
                    </v-list-tile>
                    <v-divider v-if="index + 1 < Messaggi.length" :key="`divider-${index}`"></v-divider>
                  </template>
                </v-list>
              </v-card>
            </v-flex>
          <v-flex xs12 sm6>
              <v-card>
                <v-toolbar color="green" dark>
                  <v-toolbar-title>Presenti</v-toolbar-title>
                </v-toolbar>
                <v-list two-line>
                  <template v-for="(item, index) in Giornata">
                    <v-list-tile :key="index" avatar ripple @click="">
                      <v-list-tile-content>
                        <v-list-tile-title>{{ item.headline }}</v-list-tile-title>
                        <v-list-tile-sub-title class="text--primary">{{ item.sub }}</v-list-tile-sub-title>
                        <v-list-tile-sub-title>{{ item.text }}</v-list-tile-sub-title>
                      </v-list-tile-content>
                      <v-avatar
                        color="grey lighten-4"
                      >
                        <img :src="item.avatar+index" alt="avatar">
                      </v-avatar>
                    </v-list-tile>
                    <v-divider v-if="index + 1 < Messaggi.length" :key="`divider-${index}`"></v-divider>
                  </template>
                </v-list>
              </v-card>
            </v-flex>
          </v-layout>
    </v-container>
</template>

<script>
  import  Trend  from 'vuetrend';
  export default {
    data:()=>{
      return {
        Messaggi: [
          { action: '15 min', headline: 'In Entrata',from:'Gianni Pardini', text: "Conferma della Lezione di matematica alle 15..." },
          { action: '15 min', headline: 'In Entrata',from:'Gianni Pardini', text: "Conferma della Lezione di matematica alle 15..." },
          { action: '15 min', headline: 'In Entrata',from:'Gianni Pardini', text: "Conferma della Lezione di matematica alle 15..." },
          { action: '15 min', headline: 'In Entrata',from:'Gianni Pardini', text: "Conferma della Lezione di matematica alle 15..." },
          { action: '15 min', headline: 'In Entrata',from:'Gianni Pardini', text: "Conferma della Lezione di matematica alle 15..." }
        ],
        Giornata:[
          { action: 'Studente', headline: 'Nicola Volpi', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='},
          { action: 'Studente', headline: 'Gianni Minà', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='},
          { action: 'Studente', headline: 'Gianni Minà', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='},
          { action: 'Studente', headline: 'Gianni Minà', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='},
          { action: 'Studente', headline: 'Gianni Minà', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='},
          { action: 'Studente', headline: 'Gianni Minà', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='},
          { action: 'Studente', headline: 'Gianni Minà', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='},
          { action: 'Studente', headline: 'Gianni Minà', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='},
          { action: 'Studente', headline: 'Gianni Minà', text: "Lezione di Matematica", avatar:'http://i.pravatar.cc/300?img='}]
      }
    },
    mounted(){
      
    },
    components: {
      'trend':Trend
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
#chart{
  width: 100%;
}
svg {
  height: 100%;
}
.over{

  width: 95%;
  
  left: 2.5%;
  position: absolute;
  
}
.container.grid-list-md .layout .flex{
  position: relative;
}
</style>
