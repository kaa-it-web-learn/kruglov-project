<template>
  <v-app>
    <v-navigation-drawer 
      app 
      fixed
      left
      v-model="drawer" 
      width="320"
   >
    <v-list class="hidden-md-and-up">
     <v-list-tile 
         v-for="link in links"
         :key="link.title" 
         :to="link.url" 
         >
        <v-list-tile-action>
          <v-icon color="pink">{{link.icon}}</v-icon>
        </v-list-tile-action>

        <v-list-tile-content>
           <v-list-tile-title v-text="link.title"></v-list-tile-title> 
        </v-list-tile-content>
        
      </v-list-tile> 
    </v-list> 
   </v-navigation-drawer>
    <v-toolbar app dark color="primary">
        <v-toolbar-side-icon
          @click="drawer = !drawer"
          class="hidden-md-and-up"
        ></v-toolbar-side-icon>

        <v-toolbar-title>Cистемa управления "Домофон"</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
        <v-btn 
           v-for="link in links"
           :key="link.title"
           :to="link.url"
           
           flat
        >
            <v-icon left>{{link.icon}}</v-icon> 
             {{link.title}}
        </v-btn>
        </v-toolbar-items>
   </v-toolbar>

    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  data () {
    return {
      drawer: false,
      links: [
        { title: "Login", icon: "lock", url: "/login" },
        { title: "New", icon: "note_add", url: "/new" },
        { title: "Registration", icon: "face", url: "/registration" }
      ]
    }
  }
}
</script>
