<template>
    <form v-on:submit.prevent="bookSubmit(bookTitle,bookAuthor)" action="#" method="post">
        <input v-model="bookTitle" type="text" placeholder="Enter Book:">
        <input v-model="bookAuthor" type="text" placeholder="Enter Author's name:">
        <button type="submit" name="button">Add Book</button>
    </form>
</template>

<script>

    export default {
        name: 'BookForm',
        props:['books'],
        data(){
            return{
                bookTitle : '' ,
                bookAuthor : ''
            }
        },
        methods:{
            bookSubmit(bookTitle,bookAuthor){
                this.$emit('addbook',bookTitle,bookAuthor)
            }
        }
    }

</script>

<style>

</style>
