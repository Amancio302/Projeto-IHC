<template>
  <v-row>
    <v-spacer />
    <v-spacer />
    <v-col cols="auto">
      <v-btn
        text
        block
        class="about-btn"
        href="https://ufla.br/sobre"
      >
        <div class="about-btn-text">Sobre a UFLA</div>
      </v-btn>
    </v-col>
    <v-col cols="auto">
      <v-btn
        text
        block
        class="about-btn"
        href="https://ufla.br/sobre/administracao/equipe-de-gestao"
      >
        <div class="about-btn-text">Equipe de Gestão</div>
      </v-btn>
    </v-col>
    <v-col cols="auto">
      <v-btn
        text
        block
        class="about-btn"
        href="https://ufla.br/servicos-da-ufla"
      >
        <div class="about-btn-text">Serviços da UFLA</div>
      </v-btn>
    </v-col>
    <v-col cols="auto">
      <v-btn
        text
        block
        class="about-btn"
        href="https://ufla.br/contato"
      >
        <div class="about-btn-text">Contato</div>
      </v-btn>
    </v-col>
    <v-col cols="auto">
      <v-btn
        text
        block
        class="about-btn"
        href="https://ufla.br/comunicacao/servicos1/atendimento-a-imprensa"
      >
        <div class="about-btn-text">Área de imprensa</div>
      </v-btn>
    </v-col>
    <v-spacer />
  </v-row>
</template>

<script>
export default {
  name: "About"
}
</script>

<style>
  .about-btn{
    border: hidden;
    background: transparent !important;
    max-height: 32px;;
  }
  .about-btn-text{
    font-family: "open_sansregular",'Open Sans',Arial,Helvetica,sans-serif;
    color: #ffffff;
    font-size: 1.2em;
    line-height: 19px;
    text-transform: initial;
  }
</style>