<template>
    <section>
        <div class="container">
            <div class="form">
                <div class="user signinBx">
                    <div class="imgBx"><img alt="Vue logo" src="../assets/Sign-in.jpg"></div>
                    <div class="formBx">
                        <form>
                            <h2>INICIAR SESIóN</h2>
                            <div class="inputBx">
                                <input type="text" required="requiered">
                                <span>Usuario</span>
                                <i></i>
                            </div>
                            <div class="inputBx">
                                <input type="password" required="requiered">
                                <span>Contraseña</span>
                                <i></i>
                            </div>
                            <input type="submit" value="INGRESAR">
                            <p class="signup">¿No Tienes una Cuenta? <a href="#" v-on:click="toggleForm">Registrarse</a></p>
                        </form>
                    </div>
                </div>

                <div class="user signupBx">
                    <div class="formBx">
                        <form>
                            <h2>CREAR CUENTA</h2>
                            <div class="inputBx">
                                <input type="text" required="requiered">
                                <span>Usuario</span>
                                <i></i>
                            </div>
                            <div class="inputBx">
                                <input type="text" required="requiered">
                                <span>Correo Electronico</span>
                                <i></i>
                            </div>
                            <div class="inputBx">
                                <input type="password" required="requiered">
                                <span>Contraseña</span>
                                <i></i>
                            </div>
                            <div class="inputBx">
                                <input type="password" required="requiered">
                                <span>Confirmar Contraseña</span>
                                <i></i>
                            </div>
                            <input type="submit" value="REGISTRAR">
                            <p class="signup">Tiene Cuenta <a href="#" v-on:click="toggleForm">Iniciar Secion</a>
                            </p>
                        </form>
                    </div>
                    <div class="imgBx"><img alt="Vue logo" src="../assets/Sign-up.jpg"></div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Login_Register',

    data() {
        return {
            container: null,
            section: null
        }
    },
    mounted() {
        this.container = document.querySelector('.container');
        this.section = document.querySelector('section');
    },
    methods: {
        toggleForm() {
            this.container.classList.toggle('active');
            this.section.classList.toggle('active');
        }
    }
}
</script>