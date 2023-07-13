<template>
<h1>My To Do List</h1>
<p>{{ this.prettyGreeting }} </p>
</template>

<script>
export default{
    data: function(){
        return{
            greeting: "Salutare si bine ai venit la Lista Mea",
            
        }
    },
    computed: {
        prettyGreeting: function(){
            return this.greeting + "✨"
        }
    }
    

}
</script>

<style>

</style>