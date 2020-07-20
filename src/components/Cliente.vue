<template>
    <div  id="cliente">
      <p>{{message}}</p>
      <p>RevMessage: {{revMessage}}</p>
        <!-- utilizando props -->
        <span v-bind:title="message">
            Pare o mouse sobre mim e veja a dica interligada dinamicamente!
        </span>
        <!-- renderização condicional-->
        <p v-if="seen">Agora você me viu</p>
        <!-- renderização de listas-->
        <ol>
            <li v-for="todo in todos" :key="todo.text">
                {{todo.text}}
            </li>
        </ol>
        <!-- capturando eventos, interação com usuário-->
        <button v-on:click="reverseMessage()">Inverter mensagem</button>
        <hr/>
        <!-- obs: toda vez que for alterado um elemento de tada a vue renderiza novamente -->
        <p>{{foo}}</p>
        <button v-on:click="foo = 'baz'">Change it</button>
        <!-- chaves duplas não podem ser utilizadas em atributos html, utilize a diretiva v-bind:-->
        <div v-bind:id="dynamicId"></div>
        <!-- expressões javascript-->
        {{ok ? 'sim': 'não'}}
        <br />
        {{'hello world javascript'}}
        <hr/>
    </div>
</template>
<script>
export default {
   
    data:function() {
        return {
                dynamicId:1,
                ok: false,
                rawHtml: 'html',
                foo:'foo',
                message: 'olá vue! ',
                todos: [
                        {
                            text:'aprender javascript'
                        },
                        {
                            text: 'Aprender Vue',
                        
                        },
                        {
                            text: 'Desenvolver algo incrível!'
                        }
                    ],
                seen: true,
            };
    },
    methods:{
        reverseMessage: function () {
            this.message = this.message.split('').reverse().join('');
        }
    },
    //getter-only(somente retornam valores)
    //computed usado como funções getters e posuem cache
    //exemplo: a invocação de um método sepre será feita toda vez que uma renderização ocorrer
    //enquanto isso as funções computadas somente será reavaliado quando 
    //algumas de suas dependências forem alteradas
    computed:{
        revMessage: function() {
            return this.message.split('').reverse().join('');
        }
    }
}
</script>

<style  scoped>
    h2{
        color:blue;
    }
    #cliente {
        background-color:red,
    }
</style>