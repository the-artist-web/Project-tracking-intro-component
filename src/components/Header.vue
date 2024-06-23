<template>
    <header class="header">
        <div class="container">
            <a href="#" class="logo">
                <img src="../assets/images/logo.svg" alt="img-logo">
            </a>

            <nav class="navbar" data-navbar>
                <ul class="navbar-list">
                    <li class="navbar-item">
                        <a href="#" class="navbar-link">Product</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="navbar-link">Features</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="navbar-link">Pricing</a>
                    </li>
                </ul>

                <a href="#" class="login">Login</a>
            </nav>

            <button @click="showNavbar()" class="icon-hamburger" data-icon-hamburger><img src="../assets/images/icon-hamburger.svg" alt="icon-hamburger"></button>

            <button @click="noneNavbar()" class="icon-close" data-icon-close><img src="../assets/images/icon-close.svg" alt="icon-close"></button>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
    data() {},
    methods: {
        showNavbar: function() {
            document.querySelector('[data-icon-hamburger]').classList.add("active");
            document.querySelector('[data-icon-close]').classList.add("active");
            document.querySelector('[data-navbar]').classList.add("active");
        },
        noneNavbar: function() {
            document.querySelector('[data-icon-hamburger]').classList.remove("active");
            document.querySelector('[data-icon-close]').classList.remove("active");
            document.querySelector('[data-navbar]').classList.remove("active");
        }
    }
}
</script>

<style scoped>
    .header .container {
        font-family: var(--font-family-full);
        display: flex;
        align-items: center;
        justify-content: space-between;
        text-transform: uppercase;
        height: 80px;
        width: 100%;
        position: fixed;
        top: 10px;
        left: 0;
        right: 0;
        z-index: 10;
    }
    .header .container .navbar {
        padding: 30px;
        border-radius: 6px;
        box-shadow: 0 0 20px -6px var(--Very-Dark-Blue);
        display: flex;
        flex-direction: column;
        position: fixed;
        top: 50px;
        left: 16px;
        right: 16px;
        opacity: 0;
        visibility: hidden;
        transition: .4s;
        background-color: #fff;
    }
    .header .container .navbar.active {
        top: 100px;
        opacity: 1;
        visibility: visible;
        transition: .4s;
    }
    .header .container .navbar .navbar-list {
        text-align: center;
        display: flex;
        flex-direction: column;
        padding-bottom: 30px;
        border-bottom: 1px solid var(--Grayish-Blue);
        margin-bottom: 30px;
        gap: 30px;
    }
    .header .container .navbar .navbar-list .navbar-item .navbar-link {
        font-size: 1rem;
        font-weight: 700;
        transition: .4s;
    }
    .header .container .navbar .navbar-list .navbar-item .navbar-link:hover {
        text-decoration: underline;
        transition: .4s;
    }
    .header .container .navbar .login {
        color: var(--Dark-Grayish-Blue);
        text-align: center;
        font-size: 1rem;
        font-weight: 700;
        transition: .4s;
    }
    .header .container .navbar .login:hover {
        text-decoration: underline;
        transition: .4s;
    }
    .icon-hamburger.active { display: none; }

    .icon-close { display: none; }

    .icon-close.active { display: block; } 

    /*------------------------------------------------------*\
      #ROOT
    \*------------------------------------------------------*/

    /**
     * fit size 768px
     */
    @media screen and (min-width: 768px) {
        .header .container { top: 30px; }

        .header .container .navbar {
            background-color: transparent;
            padding: 0;
            border-radius: 0;
            box-shadow: 0 0 0;
            flex-direction: row;
            position: static;
            opacity: 1;
            visibility: visible;
            gap: 100px;
        }
        .header .container .navbar .navbar-list {
            text-align: left;
            display: flex;
            flex-direction: row;
            padding-bottom: 0;
            border-bottom: transparent;
            margin-bottom: 0;
            gap: 40px;
        }
        .icon-hamburger { display: none; }
    }
</style>