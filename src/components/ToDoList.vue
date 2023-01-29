<template>
    <h1>To-Do List</h1>
    <p>Napis co chces spravit</p>

    <ul>
        <li v-for="(content, index) in characters" :key="index">
            {{ content }}
        </li>
    </ul>


    <div>
        <form @submit.prevent="characters.push(newTxt)">
      <input v-model="newTxt" type="text">
    </form>

    <p>
    {{ newTxt }}
   </p> 

    </div>
</template>

<script>
    export default {
        data() {
            return {
            newTxt:'',
            characters:[],
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>