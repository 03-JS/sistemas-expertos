## Sistemas Expertos
### 1. Define que son lenguajes imperativos y declarativos.
Un lenguaje imperativo es un lenguaje en el que se la dan instrucciones y pasos a un ordenador o máquina para que los interprete y realice.

Un lenguaje declarativo es un lenguaje en el que no se dan las instrucciones y pasos a seguir a la máquina o ordenador, si no que directamente se le da el resultado que se quiere obtener.

### 2. Crea un mapa mental con freeplane, la raiz se llamará tipos de lenguajes, con dos hijos imperativos y declarativos, añadiendo sus tipos y ejemplos de lenguajes que lo usan, por ejemplo: imperativo, OOP, Java., en cada lenguaje indica para que se usan en general en la vida real y ejemplos de aplicaciones comerciales que lo usan.
![](https://raw.githubusercontent.com/03-JS/sistemas-expertos/main/Captura%20de%20pantalla%202023-10-25%20125338.jpg)
- Java: Se utiliza principalmente para crear aplicaciones de escritorio y dispositivos móviles.
  - Ejemplos: Minecraft Java Edition, Uber.
- C#: Forma parte de la plataforma .NET de Microsoft, que sirve para crear aplicaciones multiplataforma.
  - Ejemplos: Skype para Windows Phone, Stack Overflow.
- Haskell: Este lenguaje es recomendable en tareas complejas de sectores como seguridad, tecnología financiera, blockchain y big data.
  - Ejemplos: Sigma, Cardano.
- Miranda: Lenguaje con usos similares a los de Haskell, pero que está ya algo obsoleto.
  - Ejemplos: No he podido encontrar ninguno.
- Rust: Se usa principalmente para escribir sistemas operativos.
  - Ejemplos: AWS, Microsoft, Meta y Google.
- Scheme: Es un lenguaje de propósito general.
  - Ejemplos: GIMP, SICP Mobile.
- PROLOG: Es utilizado principalmente en el campo de la inteligencia artificial.
  - Ejemplos: No he podido encontrar ninguno.
- CLIPS: Se usa principalmente para el desarrollo de sistemas expertos y aplicaciones basadas en reglas.
  - Ejemplos: No he podido encontrar ninguno.
- Fortran: Se usa para el desarrollo de aplicaciones cientıficas y el análisis numérico.
  - Ejemplos: No he podido encontrar ninguno.
- MATLAB: Es usado para el análisis de datos y su visualización, entre muchos otros.
  - Ejemplos: MATLAB Mobile, Simulink Real-Time.
- Rx.NET: Se usa para el desarrollo de aplicaciones web y el desarrollo de interfaces, entre otros.
  - Ejemplos: No he podido encontrar ninguno.
- RxJava: Tiene los mismos usos que Rx.NET.
  - Ejemplos: No he podido encontrar ninguno.

### 3. Define que es un sistema experto y que tipo de tareas se pueden resolver con él. Pon ejemplos reales de sistemas expertos, que hacen y donde se utilizan.
Un sistema experto es un sistema que emula el razonamiento actuando igual que lo haría un experto en una materia específica. Están diseñados para poder resolver problemas complejos, como el diagnóstico de enfermedades o la toma de decisiones financieras.
- Ejemplos:
  - Dendral: Es un sistema experto que se encarga de interpretar e inferir estructuras moleculares.
  - Mycin: Sistema experto encargado del diagnóstico de enfermedades infecciosas de la sangre.

### 4. ¿Qué es CLIPS?, quién lo crea, en que año, se sigue manteniendo en la actualidad, acaba de completar con datos que consideres interesantes.
CLIPS es una herramienta que provee un entorno de desarrollo para la producción y ejecución de sistemas expertos. Fue creado a partir de 1984, en el Lyndon B. Johnson Space Center de la NASA. Los fondos cesaron a principios de los años 1990, y hubo un mandato de la NASA para comprar software comercial. Actualmente, CLIPS es mantenido fuera de la NASA como software de dominio público.

### 5. ¿Cual es el futuro de los sistemas expertos con el auge de la inteligencia artificial, es decir como afectará la IA a los SE?
Yo creo que la IA podría acabar reemplazando a la mayoría de sistemas expertos, ya que seguramente será capaz de hacer la misma función de una manera más eficaz además de poder tener muchas otras funciones que podrían ayudar a las personas. No obstante, al cumplir unas funciones tan específicas, no creo que todos los sistemas expertos acaben siendo reemplazados, solo aquellos que tengan unas tareas más complejas.

### 6. En el ejemplo en rojo que puedes encontrar mas abajo, haz que el código imprima "jirafa", ¿cómo lo has hecho?
```
(deffacts hechos-iniciales
(tiene-pelos)
(tiene-pezugnas)
(tiene-rayas-negras))

(defrule mamifero-1
(tiene-pelos)
=>
(assert (es-mamifero)))

(defrule mamifero-2
(da-leche)
=>
(assert (es-mamifero)))

(defrule ungulado-1
(es-mamifero)
(tiene-pezugnas)
=>
(assert (es-ungulado)))

(defrule ungulado-2
(es-mamifero)
(rumia)
=>
(assert (es-ungulado)))

(defrule jirafa
(es-ungulado)
(tiene-cuello-largo)
=>
(printout t "Es una jirafa" crlf))
 
(defrule cebra
(es-ungulado)
(tiene-rayas-negras)
=>
(printout t "Es una cebra" crlf))
```
Para que nos imprima que es una jirafa, tenemos que modificar los hechos:
```
(deffacts hechos-iniciales
(tiene-pelos)
(tiene-pezugnas)
(tiene-cuello-largo))
```
