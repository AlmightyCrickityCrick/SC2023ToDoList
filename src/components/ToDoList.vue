<template>
<h1>My To Do List</h1>
<p>{{ this.prettyGreeting }} pentru a {{ clicks }} oara! </p>
<button @click="incrementeazaClick">Apasa-ma ca sa ma incrementezi</button>
<br>
<input type="text" v-model="itemNou">
<input type="checkbox" v-model="stareItem">
<button @click="salveazaItem">Salveaza</button>
<span>
    <p>Itemi finisati?</p>
    <input type="checkbox" v-model="stareLista">
</span>

<template v-for="i in itemi">
    <li v-if="i != undefined && stareLista == i.state">{{ i.text }}</li>
</template>

</template>

<script>

export default{
    data: function(){
        return{
            greeting: "Salutare si bine ai venit la Lista Mea",
            clicks: 0,
            itemi: [{text: "salut", state: true}],
            itemNou: "",
            stareItem: Boolean,
            stareLista: Boolean
            
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
        },

        // rescrieItem(event){
        //     console.log(event.target.value)
        //     this.itemNou = event.target.value
        // },

        salveazaItem(){
            this.itemi.push({text: this.itemNou, state: this.stareItem})
        }


    },
    beforeMount(){
        console.log("Eu ma incarc")
    },
     
    mounted(){
        console.log("Eu m-am incarcat")
    }
    

}
</script>

<style>
span{
    display: flex;
    
}
</style>