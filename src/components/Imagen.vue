<template>
    <v-row>
        <v-col v-for="item in items" v-bind:key="item.id" sm="4" cols="12">
            <v-card>
                <img :src="item.hits" v-bind="item.">
                <v-card-title>{(item.user)}</v-card-title>
            </v-card>
        </v-col>
    </v-row>
</template>
<script>
export default {
    name:'Imagen',
    props:["items"],
}
</script>