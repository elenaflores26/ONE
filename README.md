# ONE
JavaScript

# index.html
El código HTML proporciona una interfaz para una aplicación de encriptación y desencriptación de texto,
con un área de entrada de texto, botones para encriptar y desencriptar, y una sección para mostrar el resultado junto con un icono gráfico. 
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title> Challenge Encriptador</title>
    <link rel="stylesheet" href="styles.css" />
    <script src="https://unpkg.com/sweetalert/dist/sweetalert.min.js"></script>
  </head>
  <body>
    <div class="container">
      <div class="encriptar">
        <textarea
          name="texto"
          class="texto"
          id="texto"
          cols="30"
          rows="10"
          placeholder="Ingresa el texto aquí"
        ></textarea>

        <div class="terminos">
          <p>Solo letras minúsculas y sin acentos.</p>
        </div>
        <div class="botones">
          <button class="btn-encriptar" type="button" onclick="encriptar()">
            Encriptar
          </button>
          <input
            type="button"
            class="btn-desencriptar"
            value="Desencriptar"
            onclick="desencriptar()"
          />
        </div>
      </div>
      <div class="encriptado">
        <img src="img/icono.png" alt="" id="icono" />
        <div class="mensaje-encriptado" id="mensaje-encriptado">
          <h2 id="titulo-mensaje">Ningún mensaje fue encontrado</h2>
          <p id="parrafo">
            Ingresa el texto que deseas encriptar o desencriptar
          </p>
        </div>
      </div>
    </div>
  </body>
  <script src="index.js"></script>
</html>
#

#style.css
#Este código CSS define el estilo y el diseño para una aplicación web de encriptación y desencriptación de texto. #

* {
  margin: 0;
  padding: 0;
}

.container {
  position: relative;
  width: 100vw;
  height: 100vh;
  background: #efeff1;
}

.texto {
  position: absolute;
  width: 42%;
  height: 60%;
  left: 12%;
  top: 15%;
  border: none;
  font-family: "Tahoma";
  font-style: normal;
  font-weight: 400;
  font-size: 32px;
  line-height: 150%;
  background-color: #f3f5fc;
}

.texto::placeholder {
  color: #0b0a09;
}

.texto:focus,
.texto:active {
  border: none;
  outline: none;
}

.terminos {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0px;
  gap: 8px;
  position: absolute;
  width: 80%;
  left: 12%;
  top: 80%;
}

.terminos p {
  font-family: "Tahoma";
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 150%;
  color: #495057;
  opacity: 0.8;
  flex: none;
  order: 1;
  flex-grow: 0;
}

.botones {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 1% 0;
  position: absolute;
  width: 80%;
  left: 12%;
  top: 82%;
}

.btn-encriptar {
  align-items: center;
  justify-content: center;
  padding: 2%;
  gap: 8px;
  width: 25%;
  background-color: #0a3871;
  border-radius: 24px;
  font-family: "Tahoma";
  font-size: 18px;
  line-height: 19px;
  text-align: center;
  color: #fff;
}

.btn-desencriptar {
  box-sizing: border-box;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: center;
  padding: 2%;
  gap: 8px;
  width: 25%;
  background: #d8dfe8;
  border: 1px solid #0a3871;
  border-radius: 24px;
  font-family: "Tahoma";
  font-weight: 400;
  font-size: 18px;
  line-height: 19px;
  text-align: center;
  color: #0a3871;
}

.btn-desencriptar:hover,
.btn-encriptar:hover {
  margin: 0.3%;
  width: 24.5%;
  padding: 1.8%;
}

.encriptado {
  display: flex;
  justify-content: center;
  position: absolute;
  width: 30%;
  height: 90%;
  left: 60%;
  top: 5%;
  box-shadow: 0px 24px 32px -8px rgba(0, 0, 0, 0.08);
  border-radius: 32px;
}

.mensaje-encriptado {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 1%;
  gap: 16px;
  position: absolute;
  width: 100%;
  top: 65%;
  text-align: center;
}

.mensaje-encriptado h2 {
  width: 60%;
  font-family: "Tahoma";
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 120%;
  text-align: center;
  color: #343a40;
}

.mensaje-encriptado p {
  width: 80%;
  font-family: "Tahoma";
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 150%;
  text-align: center;
  color: #495057;
}

.encriptad img {
  position: absolute;
  width: 50%;
  height: 30%;
  top: 10%;
}
@media (max-width: 57.5em) {
  .container {
    display: flex;
    flex-direction: row;
  }
  .encriptar {
    width: 100%;
  }
  .texto {
    width: 80%;
    height: 60%;
    left: 10%;
    top: 5%;
  }
  .terminos {
    width: 80%;
    left: 10%;
    top: 67%;
  }
  .terminos p {
    font-size: 16px;
  }
  .botones {
    width: 80%;
    left: 10%;
    top: 70%;
  }
  .btn-encriptar,
  .btn-desencriptar {
    width: 48%;
    border-radius: 16px;
  }
  .btn-encriptar:hover,
  .btn-desencriptar:hover {
    margin: 0.3%;
    width: 47.5%;
    padding: 1.8%;
  }
  .encriptado {
    width: 80%;
    height: 15%;
    left: 10%;
    top: 80%;
  }
  .mensaje-encriptado {
    width: 100%;
    top: 5%;
  }
  .encriptado img {
    top: 0;
    display: none;
    visibility: hidden;
  }
}

# index.js
#código JavaScript define dos funciones principales, encriptar y desencriptar, que manipulan el contenido de un área de texto en una página web para encriptar o desencriptar el texto ingresado. Además, actualiza la interfaz de usuario  para reflejar el estado actual del texto procesado y muestra alertas utilizando SweetAlert.#

function encriptar() {
  let texto = document.getElementById("texto").value;
  let tituloMensaje = document.getElementById("titulo-mensaje");
  let parrafo = document.getElementById("parrafo");
  let icono = document.getElementById("icono");

  let textoCifrado = texto
    .replace(/e/gi, "enter")
    .replace(/i/gi, "imes")
    .replace(/a/gi, "ai")
    .replace(/o/gi, "ober")
    .replace(/u/gi, "ufat");

  if (texto.length != 0) {
    document.getElementById("texto").value = textoCifrado;
    tituloMensaje.textContent = "";
    parrafo.textContent = "";
    icono.src = "./img/desencrip.png";
  } else {
    icono.src = "./img/icono.png";
    tituloMensaje.textContent = "Ningún mensaje fue encontrado";
    parrafo.textContent = "Ingresa el texto que deseas encriptar o desencriptar";
    swal("Debes ingresar un texto");
  }
}

function desencriptar() {
  let texto = document.getElementById("texto").value;
  let tituloMensaje = document.getElementById("titulo-mensaje");
  let parrafo = document.getElementById("parrafo");
  let icono = document.getElementById("icono");

  let textoCifrado = texto
    .replace(/enter/gi, "e")
    .replace(/imes/gi, "i")
    .replace(/ai/gi, "a")
    .replace(/ober/gi, "o")
    .replace(/ufat/gi, "u");
  
    if (texto.length != 0) {
      document.getElementById("texto").value = textoCifrado;
      tituloMensaje.textContent = "";
      parrafo.textContent = "";
      icono.src = "./img/desencrip.png";
    } else {
      icono.src = "./img/icono.png";
      tituloMensaje.textContent = "Ningún mensaje fue encontrado";
      parrafo.textContent = "Ingresa el texto que deseas encriptar o desencriptar";
      swal( "Debes ingresar un texto");
    }
}
