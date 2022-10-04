<template>
    <div class="container-logo">
        <a href="#">
            <span class="logo">
                <img src="../assets/logo.png" style="height: 55px;">
            </span>
            <h1 class="title-logo">FARMAPAZ</h1>
        </a>
    </div>

    <div class="main">
        <div class="topbar">
            <div class="toggle" @click="collapse">
                <ion-icon name="menu-outline"></ion-icon>
                <h6 class="menu">MENÚ</h6>
            </div>
            <!-- Search -->
            <div class="search">
                <label>
                    <input type="text" placeholder="Buscar">
                    <div class="circle-search">
                        <ion-icon name="search"></ion-icon>
                    </div>
                </label>
            </div>
            <!-- userImg -->
            <div class="user">
                <img src="../assets/logo.png" alt="" srcset="">
            </div>
        </div>
    </div>

    <div class="container">
        <div class="navigation">
                <div class="hi-container">
                    <div class="toggle" @click="collapse">
                        <span class="hi-title">¡HOLA!</span>
                        <span class="hi-icon"><ion-icon name="close"></ion-icon></span>
                    </div>
                </div>
                <ul class="nav-ul">
                    <li @mouseover="activeLink">
                        <a href="#">
                            <span class="icon"><ion-icon name="home-outline"></ion-icon></span>
                            <span class="title">Inicio</span>
                        </a>
                    </li>
                    <li @mouseover="activeLink">
                        <a href="#">
                            <span class="icon"><ion-icon name="home-outline"></ion-icon></span>
                            <span class="title">Productos</span>
                        </a>
                    </li>
                    <li @mouseover="activeLink">
                        <a href="#">
                            <span class="icon"><ion-icon name="home-outline"></ion-icon></span>
                            <span class="title">Reservas</span>
                        </a>
                    </li>
                    <li @mouseover="activeLink">
                        <a href="#">
                            <span class="icon"><ion-icon name="home-outline"></ion-icon></span>
                            <span class="title">Configuraciones</span>
                        </a>
                    </li>
                    <li @mouseover="activeLink">
                        <a href="#">
                            <span class="icon"><ion-icon name="home-outline"></ion-icon></span>
                            <span class="title">Iniciar Sesion</span>
                        </a>
                    </li>
                </ul>
            <!-- </div> -->
        </div>
    </div>

    <div class="contenet">
        <Home/>
    </div>
    <!-- Footer -->
    <div class="footer-container">
        <footer class="footer footer-spacing">
                <div class="copyright text-center my-auto ">
                    <p style="text-align: center; font-size: 16px;">Copyright &copy; FARMAPAZ - NINA - 2022</p>
                </div>
        </footer>
    </div>
    <!-- End of Footer -->
</template>

<script>
import Home from './Home.vue';
    export default{
    name: "Layout",
    components: { Home },
    data() {
        return {
            toggle: null,
            navigation: null,
            main: null
        };
    },
    mounted() {
        this.toggle = document.querySelector(".toggle");
        this.navigation = document.querySelector(".navigation");
        this.main = document.querySelector(".main");
        this.contenet = document.querySelector(".contenet");
    },
    methods: {
        collapse: function () {
            this.navigation.classList.toggle("active");
            this.main.classList.toggle("active");
            this.contenet.classList.toggle("active");
        }
    }
}
</script>