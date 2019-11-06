<template>
  <v-app >
    <div class="about">
      <v-container>
        <v-row align="center" justify="center">
          <v-card app raised height="600" class="mt-5">
            <v-layout row wrap > 
              <v-flex md6 xs12>
                <v-img
                src="@/assets/images/antique-photo.jpg"
                height="600"
                >
                </v-img>
              </v-flex>
              <v-flex md6 xs12 class="leftpane">
                <v-container fluid>
                  Ama
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
  background-color: #d1cbbb;
  background-size: cover;
}
  
</style>>
