<template>
  <v-container>
      <v-layout row>
          <v-flex xs12 sm6 offset-sm3>
              <v-card>
                  <v-card-title primary-title>
                      <div>
                          <div class="headline">Wouerner Brandão</div>
                          <span class="grey--text">1,000 miles of wonder</span>
                      </div>
                  </v-card-title>
                  <v-card-text>
                    Oi, meu nome é Wouerner Brandão, nascido em 27 de Novembro de 1989, casado com Tereza Cristina, brasiliense, morador do Recanto das Emas – DF, bacharel em Sistemas de informação pela UDF no ano de 2012.

                    Busco oportunidade na área de desenvolvimento web, trabalho como desenvolvedor desde 2010.

                    Atualmente estou me capacitando como profissional em outras linguagens de programação, como: Ruby, Python e Javascript.

                    Contatos: 61-99917-9736 e o e-mail wouerner@gmail.com

                    Curriculo em PDF.
                  </v-card-text>
              </v-card>
          </v-flex>
      </v-layout>
      <v-layout
          row
          v-for="(emprego, index) in empregos"
          :key="index"
      >
          <v-flex xs12 sm6 offset-sm3>
              <v-card>
                  <v-card-title primary-title>
                      <div>
                          <div class="headline">{{emprego.empresa}}</div>
                      </div>
                  </v-card-title>
                  <v-card-text>
                    <p><strong>{{emprego.empresa}}</strong> como {{emprego.cargo}}</p>
                    <p><strong>Periodo:</strong>{{emprego.periodo}}</p>
                  </v-card-text>
              </v-card>
          </v-flex>
      </v-layout>
  </v-container>
</template>

<script>
  export default {
    data() {
        return {
            isComponentModalActive: false,
            empregos: [
                {
                    empresa: 'DataPrev',
                    cargo: 'Desenvolvedor web',
                    periodo: '13/03/2010 a 31/12/2010'
                },
                {
                    empresa: 'CEBAN',
                    cargo: 'Analista de Desenvolvimento',
                    periodo: '01/06/2011 a 31/05/2012'
                },
                {
                    empresa: 'CPM Braxis',
                    cargo: 'Programador Junior',
                    periodo: '04/06/2012 a 03/02/2013'
                },
                {
                    empresa: 'Cnec',
                    cargo: 'Analista de Desenvolvimento',
                    periodo: '20/06/2013 a 09/05/2014'
                },
                {
                    empresa: 'Cnec',
                    cargo: 'Gestão TI como Programador Pleno III',
                    periodo: '19/05/2014 a 15/01/2015'
                },
                {
                    empresa: 'CTIS - DataSUS',
                    cargo: 'Programador PHP',
                    periodo: '19/03/2015 a 13/06/2016'
                },
                {
                    empresa: 'Fundep - Ministério da Cultura',
                    cargo: 'Programador PHP',
                    periodo: '10/05/2016 a Emprego Atual',
                    colors:{
                        color: '',
                        background: 'has-background-info',
                    }
                },
            ]
        }
    },
  }
</script>

<style>

</style>
