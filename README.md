# METODOS CONSTRUCTORES - OBJETOS - CLASES 

## EJERCICIO 1 

Crear un metodo constructor llamada persona. Sus atributos son: nombre, edad y cedula. Construye los siguientes métodos para la clase:
1.1 Mostrar(): Muestra los datos de la persona. 
1.2 es_mayor_de_edad(): Devuelve un valor lógico indicando si es mayor de edad.

```javascript 
class persona(nombre, edad ,cedula){
    nombre; edad; cedula;

    constructor{
        this.nombre = nombre;
        this.edad = edad; 
        this.cedula = cedula;
    }    

    mostrar() {
        return 'Nombre: ' + this.nombre + '\nEdad: ' + this.edad + ' años \nCédula: ' + this.cedula;
    }

    es_mayor_de_edad() {
        return this.edad >= 18;
    }
}

let personita = new Persona('Maria Paula Galvis', 19, '1080222333');
console.log('mostrar', personita.mostrar());
console.log('es_mayor_de_edad', personita.es_mayor_de_edad());

```
## EJERCICIO 2

Crea un metodo constructor llamado cuenta que tendrá los siguientes atributos: titular (que es nombre de la persona) y cantidad. El titular será obligatorio y la cantidad es opcional. Construye los siguientes métodos para el metodo:
2.1 mostrar(): Muestra los datos de la cuenta.
2.2 ingresar(cantidad): se ingresa una cantidad a la cuenta, si la cantidad introducida es negativa, no se hará nada. 
2.3 retirar(cantidad): se retira una cantidad a la cuenta. La cuenta puede estar en números rojos.

```javascript 
titular = String(prompt("Ingrese Titular"));
cantidad = parseFloat(prompt("Ingrese cantidad"));

if(cant_ing > 0){
    return;
}
else{
    cantidad = Number(prompt("Ingresar cantidades positivas"));
}

class cuenta(nombre, cantidad){
    nombre; cantidad;
    
    constructor{
        this.titular = titular;
        this.cantidad = cantidad;
    }    
    
    mostrar(){
        return 'Titular: ' + this.titular + '\nValor Inicial: ' + this.cantidad;
    }
    
    ingreso(){
        cantidad1=Number(prompt("Ingrese cantidad"));
        if(cantidad1 > 0){
            this.cantidad = cantidad + cantidad1;
            return console.log("Nuevo Saldo: " + this.cantidad)
        }
        else{
            return cantidad1 = Number(prompt("Ingrese cantidades positivas"));
        }
    }
    
    retirar(){
        retiro = parseFloat(prompt("Valor a retirar"));        
        
        if(retiro > cuenta1.cantidad){
           return saldo_nuevo = cuenta1.cantidad-retiro;
        }
        else{
            return saldo_nuevo = cuenta1.cantidad-retiro;
        }
    }
}
    let cuenta1 = new cuenta(titular, cantidad);
    console.log(cuenta1.mostrar());
    console.log(cuenta1.ingreso());
    console.log(cuenta1.retirar());
    console.log('Valor Retirado: ' + retiro + '\nNuevo Saldo: ' + saldo_nuevo);
```

## EJERCICIO 3 

Crear un metodo constructor llamado formulas. Construye los siguiente metodos para la clase:
3.1 sumar(entero, entero)
3.2 fibonacci(cantidad) a partir de una entero sacar los numeros 
3.3 operacion_modulo(cantidad) a partir de una cantidad mostrar cuales dan residuo 0 
3.4 primos(cantidad) a partir de una cantidad mostrar cuales son numeros primos

```javascript 
entero1 = Number(prompt("Ingrese un Numero"));
entero2 = Number(prompt("Ingrese un Numero"));

class formulas (entero1, entero2){
    entero1; entero2;

    constructor(entero1, entero2){
    this.entero1 = entero1
    this.entero2 = entero2
    }
    
    suma(){
    suma_total= this.num1 + this.num2
    console.log("La suma es: "+suma_total)
    }

    numero = Number(prompt("Ingrese la cantidad de operaciones que desea realizar para el fibonacci"));
    
    fibonacci(){
         let numeros=[0,1];
    for (let i = 2; i < numero; i++) {
        numeros[i] = numeros[i - 2] + numeros[i - 1];
      }
        return numeros
        console.log(fibonacci(numero));
    } 
        
    operacion_modulo(){
        for (var i = 2; i < numero; i++){
            if (numero % i == 0) {
                return true;
            }
        }
        return false;
    }

    primos(){
     for (var i = 2; i < numero; i++) {

    if (numero % i == 0) {
      return false;
    }
  }
  return true;
 }

let formula1= new formulas();
   console.log(formulas.suma());    
   console.log(formulas.operacion_modulo()); 
   console.log(formulas.primos()); 
```


## EJERCICIO 4

Crear un metodo constructor llamado persona. Sus atributos son: nombre, edad, DNI, sexo (H hombre, M mujer), peso y altura Construye los siguiente metodos para la clase:
4.1 calcularIMC(): calculara si la persona esta en su peso ideal (peso en kg/(altura^2 en m)), si esta fórmula devuelve un valor menor que 20, la función devuelve un -1, si devuelve un número entre 20 y 25 (incluidos), significa que esta por debajo de su peso ideal la función devuelve un 0 y si devuelve un valor mayor que 25 significa que tiene sobrepeso, la función devuelve un 1. Te recomiendo que uses constantes para devolver estos valores.
4.2 esMayorDeEdad(): indica si es mayor de edad, devuelve un booleano. 
4.3 comprobarSexo(char sexo): comprueba que el sexo introducido es correcto. Si no es correcto, sera H.

```javascript 
nombre = String(prompt("Ingrese nombre"));
edad = parseInt(prompt("Ingrese edad"));
dni = parseInt(prompt("Ingrese DNI"));
sexo = (prompt("Ingresa H (Hombre) o M (Mujer)"));
peso = parseFloat(prompt("Ingrese peso en kg"));
altura = parseFloat(prompt("Ingrese altura en metros"));

class persona(nombre, edad,dni, sexo, peso,altura){
    nombre; edad; dni; sexo; peso; altura;

    constructor(nombre, edad, dni, sexo, peso, altura){
    this.nom = nombre;
    this.edad= edad;
    this.dni= dni;
    this.sexo= sexo;
    this.peso = peso;
    this.altura=altura;
    }
   
    calcularIMC(){
        pesoActual = persona1.peso / (Math.pow(altura, 2));
        if (pesoActual >= 20 && pesoActual <= 25) {
            return "Peso Ideal";
        } else if (pesoActual < 20) {
            return "Bajo Peso";
        } else {
            return "Sobrepeso";
        }
    }

    es_mayor_de_edad(){
        if(persona1.edad > 17){
            return true;
        }else{
            return false;
        }
       
    }
    
    Comprobar_sexo(){
        if (persona1.sexo == "H"){
            return this.sexo = "Es Hombre";
        }
        else if (persona1.sexo == "M"){
            return this.sexo = "Es Mujer";
        }
        else{
            return this.sexo = "H"
        }
    }
}

let persona1 = new persona (nombre, edad, dni, sexo, peso,altura);
console.log(persona1.calcularIMC());
console.log(persona1.esMayorDeEdad()); 
console.log(persona1.ComprobarSexo());
```

## EJERCICIO 5 

Crear un metodo constructor llamado contraseña. Sus atributos longitud y contraseña Construye los siguiente metodos para la clase:
5.1 esFuerte(): devuelve un booleano si es fuerte o no, para que sea fuerte debe tener mas de 2 mayúsculas, mas de 1 minúscula y mas de 5 números.
5.2 generarPassword(): genera la contraseña del objeto con la longitud que tenga. 
5.3 seguridadPaswword(); indicar si la contraseña es debil contiene entre 1 a 6 caracteres (caracteres numeros y letras), media (7 a 10 caracteres numeros y letras) o fuerte (11 a 20 caracteres letras y caracteres especiales)

```javascript 
contrasena = (prompt("Ingrese la contraseña a validar"));

class contraseña(){
    contraseña; longitud;

    constructor(contraseña, longitud){
        this.contrasena =contrasena;
        this.longitud=longitud;
    }
    
    es_fuerte(){
        const mayusculas = ["A", "B","C","D","E","F","G","H","I","J","K","L","M","N","Ñ","O","P","Q","R","S","T","U","V","W", "X","Y","Z"];
        let total_mayusculas = 0;
        const minusculas = ["a", "b","c","d","e","f","g","h","i","j","k","l","m","n","ñ","o","p","q","r","s","t","u","v","w", "x","y","z"];
        let total_minusculas = 0;
        const numeros = ["0", "1","2","3","4","5","6","7","8","9","0"];
        let total_numeros = 0;

        for(let i=0; i<contraseña.length; i++ ){
            if(mayusculas.includes(this.contraseña.charAt(i))){
                total_mayusculas++;
            }
            else if (minusculas.includes(this.contraseña.charAt(i))){
                total_minusculas++;
            }
            else if (numeros.includes(this.contraseña.charAt(i))){
                total_numeros++;
            }
        }

        if(total_mayusculas >2 && total_minusculas >1 && total_numeros >5){
            return true;
        }
        else{
            return false;
        }

    }
    
}

let contraseña = new contraseña(contraseña);
console.log(contraseña.esFuerte());

```


## EJERCICIO 6

Implementar un objeto que modele un contador. Un contador se puede incrementar o decrementar, recordando el valor actual. Al resetear un contador, se pone en cero.
Además es posible indicar directamente cual es el valor actual. Este objeto debe entender los siguientes mensajes:
6.1 reset() 
6.2 inc() 
6.3 dec() 
6.4 valorActual() 
6.5 valorActual(nuevoValor)


```javascript 

class contador(){
      
      crear(){
      this.valor= parseInt(prompt("Valor"));
      this.opcion = Number(prompt("Elija una Opcion\n 1- Reset\n 2- Incrementar\n 3- Decrementar\n 4- Valor"));
      switch(this.opcion){
        case 1:
          console.log('Ingrese a opcion 1');
          this.reset();
          break;
        case 2:
          console.log('Ingrese a opcion 2');
          this.increment();
          break;
        case 3:
          console.log('Ingrese a opcion 3');
          this.decrement();
          break;
        case 4:
          console.log('Ingrese a opcion 4');
          this.valor_actual();
          break;
        default:
          console.log('Ups algo ocurrio T-T');
      }
    }

    reset(){
      this.valor = 0;
      console.log(this.valor);
      return;
    }

    increment(){
      const actualizar = parseInt(prompt("Ingrese valor para incrementar"));
      this.valor= this.valor + actualizar;
      console.log("Valor actual:"+ this.valor);
      return this.valor;
    }

    decrement(){
      const actualizar = parseInt(prompt("Ingrese valor para incrementar"));
      this.valor= this.valor - actualizar;
      console.log("Valor actual:"+ this.valor);
      return this.valor;
    }
     
    valor_actual(){
        valor_actual= this.valor
        return valor_actual
    }
}
let contador_1 = new contador();
console.log(contador_1.crear());
```


## EJERCICIO 7

Agregar al contador del ejercicio 6, la capacidad de recordar un String que representa el último comando que se le dio. Los Strings posibles son "reset", "incremento", "decremento" o "actualizacion" (para el caso de que se invoque valorActual con un parámetro). Para saber el último comando, se le envía al contador el mensaje ultimoComando().
En el ejemplo del ejercicio 3, si luego de la secuencia indicada se evalúa contador.ultimoComando() el resultado debe ser "incremento"

```javascript 

```


## EJERCICIO 8

Implementar un objeto que modele a Chimuela, una dragona de la que nos interesa saber qué energía tiene en cada momento, medida en joules. En el metodo constructor simplificado que nos piden implementar, las únicas acciones que vamos a contemplar son: cuando Chimuela come una cantidad de comida especificada en gramos, en este caso adquiere 4 joules por cada gramo, y cuando Chimuela vuela una cantidad de kilómetros, en este caso gasta un joule por cada kilómetro, más 10 joules de �costo �jo� de despegue y aterrizaje. La energía de Chimuela nace en 0. El objeto que implementa este metodo constructor de Chimuela, debe entender los siguientes mensajes: 
8.1 comer(gramos) 
8.2 volar(kilometros) 
8.3 energia() 
P.ej. si sobre un REPL(Read-Eval-Print-Loop)(Lectura-Evaluación-Impresión) recién lanzado se evalúa la siguiente secuencia Chimuela.comer(100) Chimuela.volar(10) Chimuela.volar(20) Chimuela.energia() el resultado debe ser 350.

```javascript 

gr_comida=parseInt(prompt("Ingrese la cantidad en gramos de comida que le va a dar a la dragona"));
km_volar= parseInt(prompt("Ingrese la cantidad de kilometros que va a volar la dragona"));
cant_energia= 0; 
function chimuela(gr_comida,km_volar,cant_energia){
    this.comida = gr_comida;
    this.volar=km_volar;
    this.energia=cant_energia;
      this.comer= function(){
         

      }
      this.volar=function(){
        
      }
      this.energia=function(){
          this.energia = this.comida * 4
          return this.energia 

      }
```


## EJERCICIO 9

Agregar al metodo constructor de Chimuela del ejercicio 8, la capacidad de entender estos mensajes: estaDebil(), Chimuela está débil si su energía es menos de 50. 
9.1 estaFeliz(), Chimuela está feliz si su energía está entre 500 y 1000. 
9.2 cuantoQuiereVolar(), que es el resultado de la siguiente cuenta. De base, quiere volar (energía / 5) kilómetros, p.ej., si tiene 120 de energía, quiere volar 24 kilómetros. Si la energía está entre 300 y 400, entonces hay que sumar 10 a este valor, y si es múltiplo de 20, otros 15. Entonces, si Chimuela tiene 340 de energía, quiere volar 68 + 10 + 15 = 93 kilómetros. Para probar esto, sobre un REPL recién lanzado darle de comer 85 a Chimuela, así la energía queda en 10

Para saber si n es múltiplo de 20 hacer: n % 20 == 0. Probarlo en el REPL(Read-Eval-Print-Loop)(Lectura-Evaluación-Impresión)

```javascript 

```


## EJERCICIO 10

Implementar un objeto que represente una calculadora sencilla, que permita sumar, restar y multiplicar. Este objeto debe entender los siguientes mensajes:
10.1 cargar(numero) 
10.2 sumar(numero) 10.3 restar(numero) 
10.4 multiplicar(numero) 
10.5 valorActual() P.ej. si se evalúa la siguiente secuencia calculadora.cargar(0) calculadora.sumar(4) calculadora.multiplicar(5) calculadora.restar(8) calculadora.multiplicar(2) calculadora.valorActual() el resultado debe ser 24.

```javascript 

function calculadora(){
 this.crear= function(){
      this.valor= parseInt(prompt("Valor"));
      this.opcion = Number(prompt("Elija una Opcion\n 1- Sumar\n 2- Restar\n 3- Multiplicar\n 4- Valor"));
      switch(this.opcion){
        case 1:
          console.log('Usted va a sumar');
          this.sumar();
          break;
        case 2:
          console.log('Usted va a restar');
          this.restar();
          break;
        case 3:
          console.log('Usted va a multiplicar');
          this.multiplicar();
          break;
        case 4:
          console.log('Usted esta consultando el valir actual');
          this.valor_actual();
          break;

        default:
          console.log('Ups algo ocurrio T-T');
      }
    }
     this.sumar=function(){
     const actualizar = parseInt(prompt("Ingrese el numero que le quiere sumar"));   
     this.valor = this.valor + actualizar;
      console.log("Valor actual:"+ this.valor);
      return this.valor;
    }

     this.restar= function(){
      const actualizar = parseInt(prompt("Ingrese el numero que le quiere restar"));
      this.valor= this.valor -actualizar;
      console.log("Valor actual:"+ this.valor);
      return this.valor;
    }
    
     this.multiplicar= function(){
      const actualizar = parseInt(prompt("Ingrese el numero que le quiere multiplicar"));
      this.valor= this.valor *actualizar;
      console.log("Valor actual:"+ this.valor);
      return this.valor;
    }
    this.valor_actual=function(){
        valor_actual= this.valor
        return valor_actual
    }

}
let calculador_1 = new calculadora();
console.log(calculador_1.crear());

```


## EJERCICIO 11

Crear un metodo constructor llamado Libro. Sus atributos título del libro, autor, número de ejemplares del libro y número de ejemplares prestados los siguiente metodos para la clase:
11.1 Préstamo() que incremente el atributo correspondiente cada vez que se realice un préstamo del libro. No se podrán prestar libros de los que no queden ejemplares disponibles para prestar. Devuelve true si se ha podido realizar la operación y false en caso contrario. 
11.2 devolucion() que decremente el atributo correspondiente cuando se produzca la devolución de un libro. No se podrán devolver libros que no se hayan prestado. Devuelve true si se ha podido realizar la operación y false en caso contrario. 
11.3 toString() para mostrar los datos de los libros.

```javascript 

titulo_libro = String(prompt("Ingrese titulo del libro "));
autor_libro=String(prompt("Ingrese el autor del libro "));
numero_ejemplares=parseInt(prompt("Ingrese numero de ejemplares "));
numero_ejemplares_prestados=parseInt(prompt("Ingrese numero de ejemplares prestados"));

class libro(){
    titulo_libro; autor_libro; numero_ejemplares; numero_ejemplares_prestados;

    constructor(titulo_libro, autor_libro, numero_ejemplares, numero_ejemplares_prestados){
    this.titulo = titulo_libro
    this.autor = autor_libro
    this.num_ejemplares=numero_ejemplares
    this.num_ejemplares_pres=numero_ejemplares_prestados
    }


prestamo(){
    prestado= true 
    if(numero_ejemplares_prestados<numero_ejemplares){
        numero_ejemplares_prestados++;
    }
    else {
        prestado=false
    }
    return prestado

}

devolucion(){
    devuelto = true
        if (numero_ejemplares_prestados==0){
            devuelto= false

        }else {
            numero_ejemplares_prestados--;
        }
        return devuelto;
    }
    
    toString(){
        return this.titulo +" "+ this.autor+" "+this.num_ejemplares+" "+ this.num_ejemplares_pres    
    }
    
}
let crear_libro = new libro(titulo_libro,autor_libro,numero_ejemplares, numero_ejemplares_prestados);
console.log(crear_libro.prestamo());
console.log(crear_libro.devolucion());


```


## EJERCICIO 12

Se está pensando en el diseño de un juego que incluye la nave espacial Enterprise. En el juego, esta nave tiene un nivel de potencia de 0 a 100, y un nivel de coraza de 0 a 20. La Enterprise puede encontrarse con una pila atómica, en cuyo caso su potencia aumenta en 25. encontrarse con un escudo, en cuyo caso su nivel de coraza aumenta en 10. recibir un ataque, en este caso se especifican los puntos de fuerza del ataque recibido. La Enterprise �para� el ataque con la coraza, y si la coraza no alcanza, el resto se descuenta de la potencia. P.ej. si la Enterprise con 80 de potencia y 12 de coraza recibe un ataque de 20 puntos de fuerza, puede parar solamente 12 con la coraza, los otros 8 se descuentan de la potencia. La nave debe quedar con 72 de potencia y 0 de coraza. Si la Enterprise no tiene nada de coraza al momento de recibir el ataque, entonces todos los puntos de fuerza del ataque se descuentan de la potencia. La potencia y la coraza tienen que mantenerse en los rangos indicados, p.ej. si la Enterprise tien 16 puntos de coraza y se encuentra con un escudo, entonces queda en 20 puntos de coraza, no en 26. Tampoco puede quedar negativa la potencia, a lo sumo queda en 0. La Enterprise nace con 50 de potencia y 5 de coraza. Implementar este metodo constructor de la Enterprise, que tiene que entender los siguientes mensajes: 

12.1 potencia() 
12.2 coraza() 
12.3 encontrarPilaAtomica() 
12.4 encontrarEscudo() 
12.5 recibirAtaque(puntos)


```javascript 
 class Enterprise{
       
    
        inicio(){
            this.potencia=50;;
            this.coraza=5;
        }
    
    
    encontrar_pila_atomica(){
    if(this.potencia<100){
        var potExt=0
        while(potExt<25){
            if(this.potencia<100){
            
            this.potencia+=1}
    potExt+=1
    
        }
            return "subimos la potencia"
            
        
    }
    return "La potencia esta al maximo"
    
    }
    
    
    
    encontrar_escudo() {
    if(this.coraza<20){
        var coraExt=0
        while(coraExt<10){
            if(this.coraza<20){
                this.coraza+=1
            }
            coraExt+=1
                
        }
        return "subimos la coraza"
    
    }
    return "la coraza esta al maximo"
    
    }
    
    
    recibir_ataque(potenciAtaquep){
        this.potenciAtaque=potenciAtaquep
    var ataExt=0
    
        while(ataExt<(this.potenciAtaque-1)){
    
    if(this.coraza>0){
        this.coraza-=1
        
    }
    
    
    if(this.potencia>0 && this.coraza==0) {
    
        this.potencia-=1
    }
    ataExt+=1;
        }
    return `Terminaste el ataque con una potencia ${this.potencia} y con un escudo de ${this.coraza}`
    
    }
    
    
    
     mostrar_niveles(){
        return `Los niveles de Enterprise son de potencia ${this.potencia} y escudo de ${this.coraza}`
    }
    
    
    fortaleza_defensiva(){
    return this.coraza+=100
    
    }
    
    necesita_fortalecerse(){
    if(this.coraza==0&&this.potencia<20){
        return true
    }return false
    
    
    }
    
    fortaleza_ofensiva(){   
    if(this.potencia<20)
    {
        return"su ataque es de 0"
    }
    if(this.potencia>20){
        var ataque=(this.potencia-20)/2; return ataque
    return ataque
    
        }
    
    
    }
    
    }
```


## EJERCICIO 13

Agregar al metodo constructor de la Enterprise del ejercicio 12, la capacidad de entender estos mensajes. 
13.1 fortalezaDefensiva(), que es el máximo nivel de ataque que puede resistir, o sea, coraza más potencia. 
13.2 necesitaFortalecerse(), tiene que ser true si su coraza es 0 y su potencia es menos de 20. 
13.3 fortalezaOfensiva(), que corresponde a cuántos puntos de fuerza tendría un ataque de la Enterprise. Se calcula así: si tiene menos de 20 puntos de potencia entonces es 0, si no es (puntos de potencia - 20) / 2

```javascript 
class Enterprise{
       
    
        inicio(){
            this.potencia=50;;
            this.coraza=5;
        }
    
    
    encontrarPilaAtomica(){
    if(this.potencia<100){
        var potExt=0
        while(potExt<25){
            if(this.potencia<100){
            
            this.potencia+=1}
    potExt+=1
    
        }
            return "subimos la potencia"
            
        
    }
    return "La potencia esta al maximo"
    
    }
    
    
    
    encontrarEscudo() {
    if(this.coraza<20){
        var coraExt=0
        while(coraExt<10){
            if(this.coraza<20){
                this.coraza+=1
            }
            coraExt+=1
                
        }
        return "subimos la coraza"
    
    }
    return "la coraza esta al maximo"
    
    }
    
    
    recibirAtaque(potenciAtaquep){
        this.potenciAtaque=potenciAtaquep
    var ataExt=0
    
        while(ataExt<(this.potenciAtaque-1)){
    
    if(this.coraza>0){
        this.coraza-=1
        
    }
    
    
    if(this.potencia>0 && this.coraza==0) {
    
        this.potencia-=1
    }
    ataExt+=1;
        }
    return `Terminaste el ataque con una potencia ${this.potencia} y con un escudo de ${this.coraza}`
    
    }
    
    
    
     mostrarniveles(){
        return `Los niveles de Enterprise son de potencia ${this.potencia} y escudo de ${this.coraza}`
    }
    
    
    fortaleza_defensiva(){
    return this.coraza+=100
    }
    
    necesita_fortalecerse(){
    if(this.coraza==0&&this.potencia<20){
        return true
    }return false
    
    
    }
    
    fortaleza_ofensiva(){   
    if(this.potencia<20)
    {
        return"su ataque es de 0"
    }
    if(this.potencia>20){
        var ataque=(this.potencia-20)/2; return ataque
    return ataque
    
        }
    
    
    }
    
    }

```

## EJERCICIO 14
Un taller de diseño de autos quiere estudiar un nuevo prototipo. Para eso, nos piden hacer un metodo constructor concentrado en las características del motor. El prototipo de motor tiene 5 cambios (de primera a quinta), y soporta hasta 5000 RPM. La velocidad del auto se calcula así: (rpm / 100) * (0.5 + (cambio / 2)). P.ej. en tercera a 2000 rpm, la velocidad es 20 * (0.5 + 1.5) = 40. También nos interesa controlar el consumo. Se parte de una base de 0.05 litros por kilómetro. A este valor se le aplican los siguientes ajustes: Si el motor está a más de 3000 rpm, entonces se multiplica por (rpm - 2500) / 500. P.ej., a 3500 rpm hay que multiplicar por 2, a 4000 rpm por 3, etc. Si el motor está en primera, entonces se multiplica por 3. Si el motor está en segunda, entonces se multiplica por 2. Los efectos por revoluciones y por cambio se acumulan. P.ej. si el motor está en primera y a 5000 rpm, entonces el consumo es 0.05 * 5 * 3 = 0.75 litros/km. El metodo constructor debe entender estos mensajes: 
14.1 arrancar(), se pone en primera con 500 rpm. 
14.2 subirCambio() 
14.3 bajarCambio() 
14.4 subirRPM(cuantos) 
14.5 bajarRPM(cuantos) 
14.6 velocidad() 
14.7 consumoActualPorKm()

```javascript 
class motor{
    
    arrancar(){
        this.cambio=1
        this.rpm=500
    }
    
    
    subir_cambio(){
        if(this.cambio>=0 &&this.cambio<5){
    this.cambio+=1
    return this.cambio
        }return "No existe el cambio"
    }
    
    bajar_cambio() {
        if(this.cambio>=1 &&this.cambio<=5){
            this.cambio-=1
           return this.cambio
        }return "No existe el cambio"
    }
    
    subir_RPM(rpmsp) {
        this.rpms=rpmsp
        var con=0
       if(this.rpm<5000 && this.rpm>0){
             while(con<this.rpms){
                 if(this.rpm<5000){
                      this.rpm+=1
                }
                con+=1
                 
               
           }
       }return this.rpm
    }
    
    
    bajar_RPM(rpmbp){
     this.rpmb=rpmbp
        var con=0
       if(this.rpm<5000 && this.rpm>0){
             while(con<this.rpmb){
                 if(this.rpm<5000 && this.rpm>0 ){
                      this.rpm-=1
                }
                con+=1
                 
               
           }
       }return this.rpm
    
    
    }
    
    
    velocidad() {
    var velocidadT=((this.rpm/100) *(0.5+(this.cambio/2)))
        return velocidadT
    }
    
    
    consumo_actual_por_Km(kilomep){
        this.kilome=kilomep;
        var consumo=0.05*this.kilome;
    if(this.rpm>3000){
    if(this.cambio==1){
        var conExt=(this.rpm-2500)/500
    return consumo*conExt*3
    }
    if(this.cambio==2){
        var conExt=(this.rpm-2500)/500
    return consumo*conExt*2
    }
    
    var conExt=(this.rpm-2500)/500
    return consumo*conExt
    }

    return consumo
    }    
}
```# taller-7-programacion
# taller-7-programacion
# taller-7
# taller-7
