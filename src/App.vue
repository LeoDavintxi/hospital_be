<template>
  <section id="pantalla-dividida">
    <div class="izquierda">
      <div class="logIn_user">
        <div class="contenido_logIn_user">
          <h2>Registros de Usuarios</h2>
          <form>
            <input type="text" placeholder="Nombre"><br>
            <input type="text" placeholder="Apellido"><br>
            <input type="text" placeholder="Documento"><br>
            <input type="text" placeholder="Telefono"><br>
            <input type="text" placeholder="Direccion"><br>
            <button type="submit">Registrarse</button>
          </form>
        </div>
      </div>
    </div>
    <div class="derecha">

    </div>
  </section>
</template>

<script>
export default {
  name: 'App',

  data: function () {
  },

  methods: {
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
  width: 30%;
  height: 100vh;
}

.derecha {
  background: url(https://img.freepik.com/foto-gratis/mujer-control-medico-tiro-medio_23-2148934323.jpg?w=740&t=st=1663884692~exp=1663885292~hmac=30756a7d1fe43ce5c5d0c5ada5689417d090a3847567d1935f154331194f79ca);
  background-size: cover;
  width: 70%;
  height: 100vh;
}

#pantalla-dividida {
  display: flex;
}

.logIn_user {
  margin: 0;
  padding: 0%;
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;

}

.contenido_logIn_user {
  border: 3px solid #283747;
  border-radius: 10px;
  width: 80%;
  height: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.logIn_user button {
  width: 100%;
  height: 40px;
  color: #E5E7E9;
  background: #283747;
  border: 1px solid #E5E7E9;
  border-radius: 5px;
  padding: 10px 25px;
  margin: 5px 0;
}
</style>