<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-app-bar-tittle> Vue + Vuetify</v-app-bar-tittle>
      <v-spacer></v-spacer>
       <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link }}
      </v-btn>
    </v-app-bar>
    <!-- login -->
   <v-main>
    <v-card width="500" class="mx-auto mt-5">

      <v-card-tittle>
        <h1 class="display-1"> Login</h1>
      </v-card-tittle>
      <v-card-text>
        <v-form>
          <v-text-field label= "Username" prepend-icon="mdi-account-circle"></v-text-field>
          <v-text-field label= "Password" 
            prepend-icon="mdi-form-textbox-lock" 
            :append-icon="exibir ? 'mdi-eye-off' : 'mdi-eye' "
            :type="exibir ? 'text' : 'password'" 
            @click:append="exibirSenha">
          </v-text-field>
        </v-form>
      </v-card-text>
      <v-card-actions> 
        <v-btn color="success">Login</v-btn>
        <v-spacer></v-spacer>
        <v-btn color="info" >Register</v-btn>
      </v-card-actions>
    </v-card>
  </v-main>
  <v-footer
    color="primary lighten-1"
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link }}
      </v-btn>
      <v-col
        class="primary lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
    </v-row>
  </v-footer>

  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
    
    
  },
  methods: {
    exibirSenha() {
      this.exibir = !this.exibir;
    }
  },

  data: () => ({
    exibir: true, 
    links: [
        'Home',
        'Login',
        'Cadastro'
      ],
  }),
};
</script>
