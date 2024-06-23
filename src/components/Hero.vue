<template>
    <div class="hero">
        <div class="container">
            <img src="../assets/images/illustration-devices.svg" alt="illustration-devices" class="hero-img">

            <div class="hero-content">
                <p class="text">
                    <span class="new">New</span>
                    <span class="in-text">Monograph Dashboard</span>
                </p>
                <h1 class="title-content">Powerful insights<br> into your team</h1>
                <p class="text-content">Project planning and time tracking<br> for agile teams</p>
                <div class="btn-list">
                    <button class="btn-primary">Schedule a demo</button>
                    <span class="span">to see a live preview</span>
                </div>
            </div>

            <div class="bg-design"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Hero",
    data() {}
}
</script>

<style scoped>
    .hero { 
        padding: 110px 0 70px; 
        overflow: hidden;
    }
    .hero .container {
        display: flex;
        flex-direction: column;
        gap: 80px;
    }
    .hero .container .hero-img {
        position: relative;
        left: -18px;
        width: 500px;
        height: auto;
    }
    .hero .container .hero-content { font-family: var(--font-family-full); }

    .hero .container .hero-content .text {
        text-transform: uppercase;
        display: flex;
        align-items: center;
        font-size: 16px;
        font-weight: 300;
        margin-bottom: 15px;
        gap: 10px;
    }
    .hero .container .hero-content .text .in-text { 
        color: var(--Dark-Grayish-Blue);
        letter-spacing: 2px; 
        font-size: 15px;
    }
    .hero .container .hero-content .text .new {
        background-color: var(--Very-Dark-Blue);
        padding: 5px 10px;
        border-radius: 100px;
        font-weight: 600;
        color: #fff;
    }
    .hero .container .hero-content .title-content {
        text-transform: uppercase;
        font-size: 1.5rem;
        font-weight: bold;
        margin-bottom: 20px;
    }
    .hero .container .hero-content .text-content {
        color: var(--Dark-Grayish-Blue);
        font-size: 1.1rem;
        font-weight: 500;
        line-height: 1.6;
        margin-bottom: 25px;
    }
    .hero .container .hero-content .btn-list {
        display: flex;
        flex-direction: column;
        align-items: start;
        gap: 15px;
    }
    .hero .container .hero-content .btn-list .span {
        color: var(--Grayish-Blue);
        text-transform: uppercase;
        letter-spacing: 2px;
        font-weight: 300;
        font-size: 16px;
    }

    /*------------------------------------------------------*\
      #ROOT
    \*------------------------------------------------------*/

    /**
     * fit size 992px
     */
    @media screen and (min-width: 992px) {
        .hero { 
            padding: 0; 
            overflow: hidden;
        }
        .hero .container {
            align-items: center;
            justify-content: space-between;
            flex-direction: row-reverse;
            height: 100vh;
            width: 100%;
            gap: 0;
        }
        .hero .container .hero-img {
            left: auto;
            right: -350px;
            width: auto;
            height: auto;
        }
        .hero .container .hero-content .text {
            font-size: 1.1rem;
            margin-bottom: 20px;
            gap: 15px;
        }
        .hero .container .hero-content {
            position: relative;
            left: 350px;
        }
        .hero .container .hero-content .text .in-text { font-size: 14px; }

        .hero .container .hero-content .title-content {
            text-transform: uppercase;
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 20px;
            width: 800px;
        }
        .hero .container .hero-content .text-content {
            font-size: 1.2rem;
            margin-bottom: 50px;
        }
        .hero .container .hero-content .btn-list {
            flex-direction: row;
            align-items: center;
        }
    }
</style>