<template>
<div class="home">

  <h1 class="subheading">Dashboard</h1>

  <v-container class="my-5">

    <v-card class="" v-for="project in projects">

      <v-layout row wrap v-bind:class="project.status + ' pl-2'">
        <v-flex xs12 md6>

          <h1 class="caption grey--text">
            Project Title
          </h1>

          <p>
            {{project.title}}
          </p>

        </v-flex>
        <v-flex xs6 sm4  md2>

          <h1 class="caption grey--text">
            Person
          </h1>

          <p>
            Babakar
          </p>

        </v-flex>

        <v-flex xs6 sm4  md2>

          <h1 class="caption grey--text">
            Due Date
          </h1>

          <p>
            {{project.date}}
          </p>

        </v-flex>

        <v-flex xs2 sm4  md2>

          <h1 class="caption grey--text">
            Status
          </h1>

          <div>
            <v-chip small v-bind:class="project.status">   {{project.status}} </v-chip>

          </div>

        </v-flex>

      </v-layout>

      <v-divider></v-divider>

    </v-card>


  </v-container>

</div>

</template>

<script>

  export default {
    components: {

    },

    data(){
      return {

        projects:[

          {title:'Create New Website', date:'1/1/2020', status:'ongoing'},
          {title:'Train Team', date:'1/1/2019', status:'complete'},
          {title:'Launch New Business Unit', date:'1/1/2020', status:'ongoing'},
          {title:'Negotiate Contract', date:'1/1/2019', status:'overdue'}

          ]

      }
    }
  }
</script>


<style >

.ongoing{

  border-left: 4px solid orange;

}

.complete{

  border-left: 4px solid lightgreen;


}

.overdue{

  border-left: 4px solid red;


}


.v-chip.ongoing{

  background-color: orange;

}

.v-chip.complete{

  background-color: lightgreen;


}

.v-chip.overdue{

  background-color: red;


}

</style>
