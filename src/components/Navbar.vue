<template>
    <nav>
        <v-navigation-drawer v-model="drawer" app color="purple lighten-2">

            <v-layout column align-center>
                <v-flex class="mt-5">
                    <v-avatar>
                        <img
                            src="https://cdn.vuetifyjs.com/images/john.jpg"
                            alt="John"
                        >
                    </v-avatar>
                    <p class="white--text subheading mt-1">
                      mr_markin
                    </p>
                </v-flex>
                <v-flex class="mt-4 mb-3">
                    <Popup/>
                </v-flex>
            </v-layout>

            <v-list dense>
                <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-item-icon>
                        <v-icon v-text="link.icon" class="white--text"></v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title v-text="link.text" class="white--text"></v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>

            <template v-slot:append>
                <div class="pa-2">
                <v-btn color="grey lighten-1" block>Logout<v-icon right>exit_to_app</v-icon></v-btn>
                </div>
            </template>
        </v-navigation-drawer>

        <v-app-bar app flat color="grey--text">
            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="grey--text">
                <span class="font-weight-light">PHOTO</span>
                <span>Club</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            
        </v-app-bar>
    </nav>
    
</template>

<script>
export default {
  name: 'Navbar',
  components: {
 
  },
  data: () => ({
    drawer:false,
    links:[
            {icon: 'dashboard', text: 'Profile', route: '/'},
            {icon: 'folder', text: 'Trending', route: '/projects'},
            {icon: 'person', text: 'Likes', route: '/team'},
            {icon: 'person', text: 'Sign Out', route: '/team'}
          ]
  }),
};
</script>