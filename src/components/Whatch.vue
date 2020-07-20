<template>
    <div>
        <p>
            Faça uma pergunta sim/não:
            <input v-model="question">
        </p>
        <p>
            {{answer}}
        </p>
    </div>
</template>
<script>
import axios from 'axios';

export default {
    data: function () {
        return {
            question: '',
            answer: 'Eu não posso responsder até que você faça a pergunta!',
        };
    },
    methods:{
        getAnswer : function() {
            if(this.question.indexOf('?') === -1){
                this.answer = 'perguntas geralmente possui interrogação ;)';
                return;   
            }
            this.answer = 'Pensando ... ';
            axios.get('https://yesno.wtf/api')
                .then(function(response){
                    this.answer = response.data.answer === 'yes' ? 'Sim' : 'Não';

                })
                .catch(function(error){
                    this.answer = 'Error não foi possível executar a api' + error;
                })
        }
    },
    whatch:{
        question: function(){
            this.answer ='Esperando você digitar!';

        }
    }
}
</script>
<style scoped>

</style>