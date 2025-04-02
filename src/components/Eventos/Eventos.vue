<template>
    <div class="container"> 
        <div class="row mt-4">
            <div>
                <h4>Evento click</h4>
                <!-- Botón que dispara el evento click llamando al método clic() -->
                <button @click="clic" class="btn btn-danger" type="button"> Dale clic</button>
                <!-- Botón que dispara otro evento click llamando al método SoyButon() -->
                <button @click="SoyButon" class="btn btn-warning mx-2" type="button"> Dale clic 2</button>
            </div>
            <div>
                <h4>Evento Change</h4>
                <!-- Etiqueta para indicar la función del campo de entrada -->
                <label class="input-group-text" for="">Ingrese su nombre por favor </label> 
                <!-- Campo de entrada que dispara el evento change llamando al método nombreE() -->
                <input class="form-control mt-2" type="text" id="nombre" @change="nombreE">               
                <!-- Muestra el nombre ingresado en el campo de entrada -->
                <p>El nombre ingresado es: <strong>{{nombre}}</strong> </p>
            </div>

            <div>
                <h3>Evento de mouseenter y mouseleave</h3>
                <div class="text-center"
                    style="color: #ffff;  width:200px; height: 200px; background-color: black; text-align: center; padding: 15px; border-radius: 14px;" 
                    @mouseenter="mostrarMensaje" @mouseleave="OcultarMensaje">
                    <p> Pase el mouse</p>
                    <p class="text-white">{{ mensaje }}</p>
                </div>
            </div>



        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            nombre: '', // Variable para almacenar el nombre ingresado por el usuario
            mensaje: '',
        }
    },
    methods: {
        // Método que muestra una alerta cuando se presiona el botón rojo
        clic(){
            alert("Gracias por darle clic")
        },
        // Método que muestra una alerta cuando se presiona el botón amarillo
        SoyButon() {
            alert("Soy un botón")
        },
        // Método que captura el valor ingresado en el campo de texto y lo almacena en la variable nombre
        nombreE(event) {
            this.nombre = event.target.value;
        },
        mostrarMensaje(){
            this.mensaje="El mouse esta dentro del rectangulo"
        },
        OcultarMensaje(){
            this.mensaje="El mensaje está fuera del rectángulo"
        }
    }
}
</script>

<style lang="">
    
</style>