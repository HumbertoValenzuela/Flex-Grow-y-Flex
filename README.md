# Flex-Grow-y-Flex
* Uso de Flex: 1; ajustando los tamaños width usando flex

* El shorthands es flex: toma 3 parametros: 1) flex-grow 2) flex-shrink 3) flex-basis
```javascript
.contenedor {
    max-width: 1000px; /* se va a la izquierda*/
    margin: 0 auto; /*Con esto se centra*/
    border: 3px solid black;
    display: flex; /*afectan a nosotros y sidebar quedan como row pero al colocar wrap*/
    flex-wrap: wrap;/* este se va hacia abajo*/
}
@media (min-width:760px) {
    /* notar para calcular se debe sumar los flex y dividir por el width 1000/4=*/
    /* para que mida 70% y el otro 30%. colocar flex:7; y flex:3; */
    .nosotros {
        flex: 7; /*mismo tamaño 1000/2= 500px*/
        /* flex: 0 0 70%; */
    }
    .sidebar {
        flex: 3; /*mismo tamaño 500px*/
        /* flex: 0 0 70%; */
    }
}

.servicios {
    display: flex;
    flex-wrap: wrap;/* queda uno frente al otro*/
}
.servicio {
    flex: 0 0 100%;/*son 3 div -> */
    background-color: rgb(28, 245, 28);
    /* lo mismo es flex: 1; */ 
}
.doble {
    flex: 2;
    background-color: rgb(202, 64, 64);
}
@media (min-width:760px) {

.servicio {
    flex: 1 0 0px;/*son 3 div -> */
    background-color: rgb(255, 75, 9);
    /* lo mismo es flex: 1; */ 
}
.doble {
    flex: 2;
    background-color: rgb(240, 42, 42);
}
}
```
