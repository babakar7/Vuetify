<template>

<div>

<v-toolbar app>

  <v-toolbar-side-icon v-on:click="drawer = !drawer">

  </v-toolbar-side-icon>

  <v-toolbar-title>
    <span> Manager  </span>
  </v-toolbar-title>

  <v-spacer>
  </v-spacer>

  <v-btn depressed>
    <span>Sign Out</span>
    <v-icon>exit_to_app</v-icon>
  </v-btn>

</v-toolbar>

<v-navigation-drawer class="primary" app v-model="drawer">

  <v-list v-for="item in links" v-bind:key="item.title">


    <v-list-tile router v-bind:to="item.route">
      <v-list-tile-action>
        <v-icon class="white--text">{{item.icon}}</v-icon>
      </v-list-tile-action>
      <v-list-tile-content >
        <v-list-tile-title  class="white--text">{{item.title}}</v-list-tile-title>
      </v-list-tile-content>
    </v-list-tile>


  </v-list>

</v-navigation-drawer>

</div>

</template>
<script>

  export default {
    data(){
      return{
        drawer:false,
        links:[{title:"Dashboard", icon:'dashboard', route:'/'},
        {title:"My projects", icon:'folder', route:'/projects'},
        {title:"Team", icon:'person', route:'/team'}]

      }
    }
  }
</script>
