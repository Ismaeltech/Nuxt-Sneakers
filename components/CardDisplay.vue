<template>
    <div class="container">
        <h2 class="header">
            Trending
        </h2>
        <button class="all-btn">See All</button>
        <div class="cards-container">
            <img class="sneaker" src="" alt="">
            <h4 class="title"></h4>
            <p class="from">From</p>
            <p class="price"></p>
            <p class="from">on</p>
            <img class="brand" src="" alt="">

        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                products: null
            };
        },
    methods: {
        async getData() {
            try {
                var options = {
                    method: 'GET',
                    headers: {
                        'accept': 'application/json'
                    }
                };
                const SneaksAPI = require('sneaks-api');
                const sneaks = new SneaksAPI();
                sneaks.getProducts("Yeezy Cinder", (err, products) => {
                    console.log(products);
                  })
                const response = await fetch("https://sneaks-api.azurewebsites.net",options);

                this.data = await response.json();
                console.log(this.data)
            } catch (error) {
                console.log(error); 
            }
        },
    }
    }
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Barlow:wght@800&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Barlow', sans-serif;
}


</style>