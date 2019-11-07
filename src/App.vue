<template>
  <v-app >
    <div class="about">
      <v-container>
        <v-row align="center" justify="center">
          <v-card app raised height="600" class="mt-5">
            <v-layout row wrap > 
              <v-flex md6 xs12 class="d-none d-sm-flex">
                <v-img
                src="@/assets/images/antique-photo.jpg"
                height="600"
                >
                </v-img>
              </v-flex>
              <v-flex md6 xs12 class="leftpane">
                <v-container fluid>
                  <v-layout row wrap class="pa-5 ma-10">
                    <v-flex md12 xs12 class="mt-10"> 
                      <span class="display-1 font-weight-bold GothamBold brown--text">Welcome!</span>
                      <br>
                      <span>Sign in to continue</span>
                    </v-flex>
                    <v-flex>
                      <v-text-field
                        v-model="name"
                        :rules="nameRules"
                        label="Name"
                        required
                        color="brown"
                      ></v-text-field>
                      <v-text-field
                        v-model="password"
                        :rules="nameRules"
                        label="Password"
                        type="password"
                        required
                        color="brown"
                      ></v-text-field>
                      <v-btn class="mr-4 white--text" @click="submit" color="brown" >Login</v-btn>
                    </v-flex>
                  </v-layout>
                </v-container>               
              </v-flex>
            </v-layout>
          </v-card>
        </v-row>
      </v-container>    
    </div> 
  </v-app> 
</template>

<script>
export default {
  
}
</script>

<style scoped>

@font-face {
  font-family: GothamBook;
  src: url("assets/fonts/Gotham-Font/GothamBook.ttf");
}

@font-face {
  font-family: GothamMedium;
  src: url("assets/fonts/Gotham-Font/GothamMedium.ttf");
}

@font-face {
  font-family: GothamBold;
  src: url("assets/fonts/Gotham-Font/GothamBold.ttf");
}

.about{
  /* The image used */
  background-image: url("assets/images/antique-photo.jpg")!important;

  /* Full height */
  height: 100vh;

  /* Center and scale the image nicely */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;

  font-family: GothamBook;
}

.leftpane{
  background-color: #cfcdc0;
  background-size: cover;
}

.GothamBold{
  font-family: GothamBold;
}


  
</style>>
