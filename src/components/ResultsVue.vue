<template>
  <div>
    <p>Seu tempo de reação foi de <span v-text="this.score"></span> milisegundos.</p>
  </div>
  <span class="rank" v-text="this.rank"></span>

</template>

<script>

export default {   
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score > 250) {
                this.rank = "Você está na média de geral aqui!"
            }else if (this.score <= 250) {
                this.rank = "Você tem dedos de ninja!"
            }

            //     this.rank = "Olha, sensacional! Superou os ninjas!"
            //     this.rank = "Você é o master clicker do faroeste virtual!"
            //     this.rank = "Você é um(a) Deus(a) do click! Todos te veneram"
            //     this.rank = "Seu nome ficará gravado na história deste game..."
    }   

}
</script>

<style>
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>