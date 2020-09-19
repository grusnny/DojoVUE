<template>
    <v-container>
        <v-text-field
            label="Escribe tu texto"
        ></v-text-field>
        <div>
        <v-btn small color="primary" @click="searchitem">Primary</v-btn>
        </div>
    </v-container>
</template>>
<script>
import axios from 'axios';
export default {
    name:'Search',
    data:()=>({
        search:[],
        word:'',
    }),
    methods:{
        searchItem(){
            axios
            .get("https://pixabay.com/api/?key=18325849-94cafec8b0f30985ae8cfbdde&q="+this.word+"&image_type=photo ")
            .then(response=>{
                    this.search=response.data;
                    this.$emit("searchResult",response.data);
            });
        }
    }
}
</script>