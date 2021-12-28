<template>
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
</template>

<script>


export default ({

  data: () => ({
    exibir: true, 
    links: [
        'Home',
        'Login',
        'Cadastro'
    ],
  }),
  methods: {
    exibirSenha() {
      this.exibir = !this.exibir;
    }
  },
});
</script>

<style scoped>

</style>
