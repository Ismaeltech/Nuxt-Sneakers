<template>
    <div class="Hero">
        <div class="text-container">
            <div class="info">
            <h1>HighendSneakers</h1>
            <p class="text">Open Your Doors and Explore</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
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

p {
    font-size: 28px;
    font-weight: 700;
}

.Hero {
    width: 100%;
    height: 100vh;
    background: linear-gradient(rgba(0, 0, 0, 0.400), rgba(0, 0, 0, 0.400)), url("~assets/images/jordan.jpg") no-repeat center / cover;
    color: white;
}

.text-container {
    width: 90%;
    height: 100%;
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    align-content: center;
    justify-content: center;
}

.text-container .info h1 {
    font-size: 8rem;
    font-weight: 900;
    margin-bottom: 2.5rem;
}

.text-container .info p {
    font-size: 3.2rem;
    font-weight: 900;
}

.text {
    display: flex;
    align-content: center;
    justify-content: center;
}

.info {
    margin-top: 12rem;
}
</style>