<template>
    <div class="projetos">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <h2>Meus Projetos</h2>
                </div>

                <div class="container">
                    <div class="row-projetos">
                        <div v-for="projeto in projetos" :key="projeto.nome" class="projeto text-center">
                            <h4>{{ projeto.nome }}</h4>
                            <div class="embed-responsive embed-responsive-16by9">
                                <video class="embed-responsive-item" controls>
                                    <source :src="require(`../assets/projects/${projeto.video}.mp4`)" type="video/mp4">
                                    Seu navegador não suporta a tag de vídeo.
                                </video>
                            </div>
                            <p>{{ projeto.texto }}</p>
                        </div>
                    </div>
                </div>


            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'

@Options({
    components: {}
})
export default class Projetos extends Vue {

    projetos = [
        {
            nome: 'Spotify Clone',
            video: 'spotify_clone',
            texto: 'Um app tipo Spotify bem dinâmico feito em VueJS e PHP que permite login e cadastro de usuários, e que salvem músicas em suas respectivas playlists.'
        },

        {
            nome: 'Maragogi',
            video: 'maragogi',
            texto: 'Um projeto front-end feito em VueJS que mostra detalhes sobre Maragogi - AL'
        },

        {
            nome: 'Itália Tour',
            video: 'italia_tour',
            texto: 'Um projeto feito em VueJS e em NodeJS com TypeScript que permite agendar passeios pela Itália (Ex: Roma, Veneza, Milão)'
        },

        {
            nome: 'Pluug-ai Sistema',
            video: 'pluug_ai_sistema',
            texto: 'O front-end estático do sistema da Pluug-ai feito em HTML5, CSS3, Bootstrap e JavaScript'
        },

        {
            nome: 'Turbo Digital',
            video: 'turbo_digital',
            texto: 'O site do Turbo Digital, feito em React, NextJS e Tailwind, onde ensina como se posicionar, criar conteúdo e vender com estratégia!'
        },

        {
            nome: 'Inova Option',
            video: 'inova-option',
            texto: 'O site do Inova Option, feito em VueJS, SCSS e Bootstrap, onde o cliente pode negociar ações, forex e criptomoedas'
        },

        {
            nome: 'Umuarama',
            video: 'umuarama',
            texto: 'Um projeto feito em HTML5, CSS3, Bootstrap e JavaScript, que mostra detalhes sobre Umuarama'
        },

        {
            nome: 'Eder Notícias',
            video: 'eder_noticias',
            texto: 'Um portal de notícias feito em HTML5, CSS3, Bootstrap e JavaScript'
        },

        {
            nome: 'Notifish',
            video: 'notifish',
            texto: 'Um sistema feito em HTML5, CSS3, Bootstrap e JavaScript, o qual facilita o processo de comunicação tomando o papel de um mediador entre você e o WhatsApp'
        }
    ]

}
</script>

<style lang="scss">
@import '../scss/portfolio.scss';
</style>