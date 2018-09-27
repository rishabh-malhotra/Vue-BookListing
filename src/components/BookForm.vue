<template>
    <form v-on:submit.prevent="bookSubmit(bookTitle,bookAuthor)" class="" action="#" method="post">
        <input v-model="bookTitle" type="text" placeholder="Enter Title">
        <input v-model="bookAuthor" type="text" placeholder="Enter Author">
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
                this.$emit('addBook',bookTitle,bookAuthor)
            }
        }
    }

</script>

<style>

</style>
