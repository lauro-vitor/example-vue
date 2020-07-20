<template>
  <div id="app">
   <InitialComponent title="title" post="posts"/>
  </div>
</template>

<script>
import InitialComponent from './components/InitialComponent';
//import BlogPost from './components/BlogPost'
//import HeaderPost from './components/HeaderPost'
//import BlogRow from './components/BlogRow'

//import Formularios from './components/Formularios'
//import Todos from './components/Todos'
//import Listas from './components/Listas'
//import Cliente from './components/Cliente'
//import Whatch from './components/Whatch'
//import Condicional from './components/Condicional'
export default {
  name: 'App',
  components: {
    InitialComponent
  },
  data: () => ({
    posts:[
      {id: 1, title: 'Title Post 1', post:'post 1'},
      {id: 2, title: 'Title Post 2', post:'post 2'},
      {id: 3, title: 'Title Post 3', post:'post 3'},
      {id: 4, title: 'Title Post 4', post:'post 4'},
    ]
  }),
}
</script>

<style>
</style>
    <!-- <HeaderPost />
    <BlogPost
      v-for="post in posts"
      v-bind:key="post.id"
      v-bind:title="post.title"
      v-bind:post="post.post"
       /> -->
    <!-- <InitialComponent title="Titulo exemplo" post="exemplo de post"/> -->
    <!-- <Formularios /> -->
    <!-- <Todos /> -->
    <!-- <Listas /> -->
    <!-- <Cliente message="props"/> -->
    <!-- <Condicional /> -->

  <!--  //BlogPost,
    //HeaderPost
    //InitialComponent
    //Formularios
    //Todos,
    //Listas,
     //Condicional,
    //Cliente,
    //Whatch, -->
 <!--<HeaderPost />
    <table>
      <tr is="BlogRow">
       <BlogPost
        v-for="post in posts"
        v-bind:key="post.id"
        v-bind:title="post.title"
        v-bind:post="post.post"
       />
      </tr>
    </table> -->