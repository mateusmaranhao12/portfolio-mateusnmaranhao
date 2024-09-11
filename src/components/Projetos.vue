<template>
    <div class="projetos">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <h2>Meus Projetos</h2>
                </div>

                <div class="col-md-12">
                    <div class="row">
                        <div v-for="projeto in projetos" :key="projeto.nome"
                            class="col-sm-12 col-md-4 col-lg-4 projeto text-center mb-5">
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
        }
    ]

}
</script>

<style lang="scss">
@import '../scss/portfolio.scss';
</style>