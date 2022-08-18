<template>
  <v-row  justify="center" class="space px-16">
    <v-col cols="12" xs="12" sm="6" md="4" v-for="(product, i) in products" :key="i">
        <v-card class="mx-auto rounded-x1" max-width="300" flat outlined>
            <div align="center" justfy="center">
                <v-img max-height="300" max-width="300" contain :src="product.img"></v-img>
            </div>
            <v-card-title>{{product.title}}</v-card-title>
            <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{product.subtitle}}</v-card-title>
            <v-card-title class="mt-n4">{{product.price}}</v-card-title>
            <v-card-actions class="mw-2 mt-n4">
                <v-btn outlined class="mt-n2 add">
                    <v-icon color="green" @click="decrement">mdi-minus</v-icon>
                </v-btn>

                <v-spacer></v-spacer>
                <v-btn class="mx-2 mt-n3" fab dark small color="green">
                
                    <v-icon dark>mdi-shopping</v-icon>
                </v-btn>
            </v-card-actions>
        </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
    data: () => ({
        bpm:1,
        products: [
            { img: "1.png", title: "Cabbage", subtitle: "1kg", price: "$12"},

            { img: "1.png", title: "Cabbage", subtitle: "1kg", price: "$12"},

            { img: "1.png", title: "Cabbage", subtitle: "1kg", price: "$12"},

            { img: "1.png", title: "Cabbage", subtitle: "1kg", price: "$12"},

            { img: "1.png", title: "Cabbage", subtitle: "1kg", price: "$12"},
        
            { img: "1.png", title: "Cabbage", subtitle: "1kg", price: "$12"},
        ]
    }),

    methods: {
        decrement() {
            this.bpm--
        },
        increment() {
            this.bpm++
        }
    }
}
</script>

<style>

</style>