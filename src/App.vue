<template>
  <v-app id="inspire">
  <v-card
    color="grey lighten-4"
    flat
    height="200px"
    tile
  >

  <v-btn><router-link to="/hello">HelloWorld</router-link></v-btn>
    <v-toolbar dense>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>
  </v-card>

    <v-content>
      <router-view></router-view>
      <v-container
        fluid
        fill-height
      >
        <v-layout
          align-center
          justify-center
        >
          <v-flex
            xs12
            sm8
            md4
          >
         <router-link to="/hello">Go to Hello</router-link>
            <v-card class="elevation-12">
              <v-toolbar
                color="primary"
                dark
                flat
              >
                <v-toolbar-title>Face Recogniton Report System </v-toolbar-title>
                <v-spacer></v-spacer>
              </v-toolbar>
              <v-card-text>
                <v-form>
                
                  <v-text-field
                    prepend-icon="person"
                    label="Username"
                    v-model="username"
                    type="text"
                  ></v-text-field>

                  <v-text-field
                   prepend-icon="lock"
                    id="password"                  
                    label="Password"
                    v-model="password"
                    type="password"
                  ></v-text-field>
                   <v-spacer></v-spacer>
                <v-btn id="submit" color="red" @click="submit">Login</v-btn>
                </v-form>
              </v-card-text>
              <v-card-actions>
               
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data(){
    return{
      username:"",
      password:""

    }
  },
  methods:{
    submit:function(){

           this.$router.push('/hello')
    }
  }
}
</script>

<style scoped>
#submit{
  margin-left: 200px;
}

</style>


