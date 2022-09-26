<template>
    <section id="pantalla-dividida">
        <div class="izquierda">
        </div>
        <div class="derecha">
        </div>
    </section>
</template>
  
<script>
import axios from 'axios';
export default {
    name: 'consultaPacientes',

    data: function () {
        return {
            usuario: {
                nombre: "",
                apellido: "",
                direccion: "",
                correo: "",
                user_name: "",
                password: "",
                id_registro: "1"
            }
        }
    },

    methods: {
        registroUsuario: function (event) {
            const url = "http://127.0.0.1:8000/user/";
            axios.post(url, this.usuario)
                .then((result) => {
                    alert("Registro Exitoso: " + result.status);
                    event.target.reset();
                })
                .catch((error) => {
                    alert("ERROR: Fallo en el registro: " + error);
                });
        }
    },

    created: function () {
    }
}
</script>
  
<style>
body {
    margin: 0 0 0 0;
}

.izquierda {
    background: white;
    width: 40%;
    height: 100vh;
}

.derecha {
    background: url(https://img.freepik.com/foto-gratis/mujer-control-medico-tiro-medio_23-2148934323.jpg?w=740&t=st=1663884692~exp=1663885292~hmac=30756a7d1fe43ce5c5d0c5ada5689417d090a3847567d1935f154331194f79ca);
    background-size: cover;
    width: 60%;
    height: 100vh;
}

#pantalla-dividida {
    display: flex;
}

.logo {
    width: 40%;
}

.logIn_user {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.contenido_logIn_user {
    border: 2px solid #283747;
    border-radius: 20px;
    width: 80%;
    height: 80%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: white;
}

.logIn_user button {
    width: 100%;
    height: 40px;
    color: #E5E7E9;
    background: #283747;
    border-radius: 5px;
    padding: 0px 0px;
    margin: 0px 0px;
}

.contenido_logIn_user h5 {
    text-align: center;
}

.forma input{
    width: 100%;
}

select{
    width: 100%;
}
</style>