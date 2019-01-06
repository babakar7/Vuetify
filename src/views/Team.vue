<template>
  <div class="team">

    <h1 class="subheading"> Team </h1>

    <v-container class="my-5" >
      <v-layout row wrap justify-space-between>

        <v-flex xs12 sm6 md4 lg3 v-for="person in team">

          <v-card>

            <v-card-text>
              <div>
                <p class="subheading">{{person.name}}</p>
                <p>{{person.role}}</p>
              </div>

            </v-card-text>

            <v-card-actions>
              <v-btn depressed>
                <v-icon>message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>

</template>


<script>
  export default {
    data(){
      return {
          team:[{name:'Babakar', role:'Web Developer'},
        {name:'Amy', role:'Lead Developer'},
      {name:'Max', role:'Web Designer'}]
      }
    }
  }
</script>
