<template>
<div>
    <b-navbar toggleable="lg" type="light">
      <div class="container">
        <b-navbar-brand href="#">NonStopGaming</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <li class="nav-item">
              <router-link class="nav-link" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/games">Games</router-link>
            </li>

       </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
  
  <v-app id="inspire">
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="8">
            <v-card class="elevation-12">
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 green--text text--light-1"
                        >Log in to NonStopGaming</h1>
                        <h4 class="text-center mt-4 green--text text--light-1">Log in with your account</h4>
                        <v-form>
                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                            color="teal accent-3"
                          />

                          <v-text-field
                            id="password"
                            label="Password"
                            name="password"
                            prepend-icon="lock"
                            type="password"
                            color="teal accent-3"
                          />
                        </v-form>
                      </v-card-text>
                      <div class="text-center mt-3">
                         <router-link to="/">
              
                          
                        <v-btn rounded color="green light -1" dark>LOG IN</v-btn> 
                        <br>
                        </router-link>
                      </div>
                      <div class="text-center mt-3">
                         <router-link to="/admin">
              
                          
                        <v-btn rounded color="green light -1" dark>ADMIN</v-btn>
                        <br>
                        <br>
                        </router-link>
                      </div>
                    </v-col>
                    <v-col cols="12" md="4" class="green light -1">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">First Time Visit?</h1>
                        <h5
                          class="text-center"
                        >Get your account here</h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined dark @click="step++">REGISTER</v-btn>
                      </div>
                      
                    </v-col>
                  </v-row>
                </v-window-item>
                <v-window-item :value="2">
                  <v-row class="fill-height">
                    <v-col cols="12" md="4" class="green light -1">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Have an acoount?</h1>
                        <h5
                          class="text-center"
                        >Log in here</h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined dark @click="step--">Log in</v-btn>
                      </div>
                    </v-col>

                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1 class="text-center display-2 green--text text--light-1">Create Account</h1>
                        <h4 class="text-center mt-4 green--text text--light-1">Enter your email for registration</h4>
                        <v-form>
                          <v-text-field
                            label="Name"
                            name="Name"
                            prepend-icon="person"
                            type="text"
                            color="teal accent-3"
                          />
                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                            color="teal accent-3"
                          />

                          <v-text-field
                            id="password"
                            label="Password"
                            name="password"
                            prepend-icon="lock"
                            type="password"
                            color="teal accent-3"
                          />
                        </v-form>
                      </v-card-text>
                      <div class="text-center mt-n5">
                        <router-link to='/'>
                        <v-btn rounded color="green light -1" dark>REGISTER</v-btn>
                        </router-link>
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
              </v-window>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</div>
</template>

<script>
export default {
  data: () => ({
    step: 1
  }),
  props: {
    source: String
  }
};
</script>