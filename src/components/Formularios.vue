<template>
    <div>
        <form action="" v-on:submit.prevent="submitForm()">
            <input type="text" v-model="name" placeholder="nome">
            <p></p>
            <input type="text" v-model="lastName" placeholder="sobre nome"> 
            <p></p>
            <input type="text" v-model="email" placeholder="email@exemplo.com"/>
            <p></p>
            <select name="" id="" v-model="selectedState">
                <option 
                    v-for="optionsItem in options" 
                    v-bind:key="optionsItem"
                    v-bind:value="optionsItem"
                    >
                    {{optionsItem}}
                </option>
            </select>
            <p></p>
            <button type="submit">Enviar</button>
        </form>
    </div>
</template>
<script>
export default {
    data: () => ({
        name: '',
        lastName: '',
        email: '',
        selectedState: 'ES', //sempre colocar os valores so selected aqui
        options : [
            'ES',
            'MG',
            'SP',
            'RJ'
        ],
    }),
    methods: {
        submitForm: function (){
            console.log('name', this.name);
            console.log('lastName', this.lastName);
            console.log('email', this.email);
            console.log('selectedState', this.selectedState);
            alert('ok')
        }
    }
}
</script>
<style scoped>

</style>