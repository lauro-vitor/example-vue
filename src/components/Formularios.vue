<template>
    <div>
        <form action="" v-on:submit.prevent="submitForm()">
            <CustomInput placeHolder="nome" v-model="name"/>
            <!-- <input type="text" v-model="name" placeholder="nome"> -->
            <p></p>
            <CustomInput placeHolder="sobre nome" v-model="lastName" />
            <!-- <input type="text" v-model="lastName" placeholder="sobre nome"> _-->
            <p></p>
            <CustomInput placeHolder="email@exemplo.com" v-model="email" />
            <!-- <input type="text" v-model="email" placeholder="email@exemplo.com"/> -->
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
 import CustomInput from './CustomInput'
export default {
    components:{
        CustomInput
    },
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