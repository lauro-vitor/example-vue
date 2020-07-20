<template>
    <div>
        <!-- numeros filtrados -->
        <div>
            <ul>
                <li v-for="n in evenNumbers" v-bind:key="n">
                    {{n}}
                </li>
            </ul>
        </div>
        <!-- iterando uma lista de objetos -->
        <div >
            <ul>
                <li v-for="listItem in listObject" v-bind:key="listItem.email">
                    {{listItem.fullName}} - {{listItem.email}}
                </li>
            </ul>
        </div>
        
        <hr>
         <!-- iterando um objeto -->
        <div  v-for="(value, name, index) in object" v-bind:key="value.title">
          {{index}} . {{name}}: {{value}}
        </div>
        <ul>
            <!-- renderização de um array comum -->
           <li v-for="message in messages" v-bind:key="message">
               {{message}}
           </li>
        
        </ul>
        
    </div>
</template>

<script>
export default {
    computed:{
        evenNumbers: function() {
            return this.numbers.filter(number => number % 2);
        },
    },
    data: () => ({
        numbers:[1, 2, 3, 3, 4, 5, 6, 7, 8, 9, 10],

        listObject:[
            {
                email: 'fulano@exemplo.com',
                fullName: 'fulano'
            },
            {
                email: 'beltrano@exemplo.com',
                fullName: 'beltrano'
            },
            {
                email: 'ciclano@exemplo.com',
                fullName: 'ciclano'
            },  
            {
                email: 'eu@email.com',
                fullName: 'Eu'
            },  
            {
                email: 'zezionho@email.com',
                fullName: 'zezinho'
            },  
            {
                email: 'exemplo@email.com',
                fullName: 'Exemplo'
            }
        ],
        object:{
            title: 'Como renderizar Listas no Vue',
            author: 'Jane Doe',
            publishedAt: '2016-04-10'
        },
        messages:[
            'oi tudo bem ?',
            'sim e você?',
            'tudo certo ',
            'OK'
        ]
    }),
}
</script>
<style scoped>

</style>