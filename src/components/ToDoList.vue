<template>
<h1>My To Do List</h1>
<p>{{ this.prettyGreeting }} pentru a {{ clicks }} oara! </p>
<button @click="incrementeazaClick">Apasa-ma ca sa ma incrementezi</button>
</template>

<script>
export default{
    data: function(){
        return{
            greeting: "Salutare si bine ai venit la Lista Mea",
            clicks: 0
            
        }
    },
    computed: {
        prettyGreeting: function(){
            return this.greeting + "✨"
        }
    },
    methods: {
        incrementeazaClick(){
            this.clicks++;
        }

    }
    

}
</script>

<style>

</style>