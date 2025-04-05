<template>
    <Sobre />
    <Conhecimentos />
    <Projetos />
    <Contato />
</template>

<script lang="ts">
import Conhecimentos from '@/components/Conhecimentos.vue';
import Contato from '@/components/Contato.vue';
import Projetos from '@/components/Projetos.vue';
import Sobre from '@/components/Sobre.vue';
import { Options, Vue } from 'vue-class-component'

@Options({
    components: {
        Conhecimentos,
        Contato,
        Projetos,
        Sobre
    },
})
export default class Portfolio extends Vue { }
</script>