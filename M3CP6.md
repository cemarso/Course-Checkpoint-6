# **CheckPoint 6 – Preguntas teóricas**

#### **¿Para qué usamos Clases en Python?**    

Las clases en Python son estructuras de programación que definen objetos mediante métodos (funciones) y atributos (variables). Los objetos son conjuntos de funciones y variables. Se usan en la técnica de programación orientada a objetos. 
Las clases en Python sirven para organizar el código de nuestros programas haciéndolo más legible y separado en bloques funcionales reutilizables y que pueden heredarse, ahorrando código y facilitando su mantenimiento. 
Se pueden crear clases base y clases derivadas de ellas. Los métodos de clases derivadas pueden llamar a métodos de sus clases base con el mismo nombre. Y los métodos definidos en las clases derivadas sobrescriben los métodos de sus clases base. 

Sintaxis:

La clase se define mediante la palabra clave ‘class’ seguido del nombre de la clase y dos puntos.
Las clases definen un modelo para crear objetos que son instancias de esas clases, es decir, la instancia de la clase consiste en crear un objeto mediante esa clase, el cual se almacena en una variable. La instanciación de clases emplea la misma notación que las funciones. El objeto es una función sin parámetros que devuelve una instancia. 

```sh
class ClassName: 

   def function(self):
       return 'text'
    

instantiation = ClassName()
print(instantiation.function())
```

La sintaxis para llamar a la función contenida en la clase es:

```sh
instantiation.function()
```

El cuerpo de la clase es donde se definen métodos y atributos. Los métodos son funciones definidas dentro de la clase, y los atributos son variables definidas dentro de la clase. 
Los métodos contenidos en las clases deben tener siempre un primer argumento por defecto llamado ‘self’ que hace referencia a la instancia, es decir, que representa al objeto creado. Y puede haber o no más argumentos.

```sh
def nombre_metodo(self, argumentos)
```

La sintaxis de los atributos es:

```sh
self.nombre_atributo = valor
```

#### **¿Qué método se ejecuta automáticamente cuando se crea una instancia de una clase?**

Cuando se crea una instancia de clase se invoca automáticamente al método dunder init. Esta función se llamará automáticamente cada vez que se cree una instancia de la clase y procesará lo que esté contenido dentro de ella. 
Cuando se crea una clase y se llama a un objeto mediante instanciación, Python llama al método dunder new para crear el objeto vacío. El método new es un método de clase que no necesita instanciación para ser llamado y tampoco necesita el argumento self ya que no pertenece al objeto de la clase. El estado inicial de los atributos del objeto se definirá dentro la clase llamando al método dunder init.

Por ejemplo, dentro de la clase Results tenemos una función init definida que añade a la clase los datos que se pasan como argumentos y se asignan al objeto creado en la instanciación. Después, se define una función que retorna dichos datos en un string. Finalmente, se crea una instancia, un objeto de la clase Results. Creamos la variable cecilia que contendrá los resultados con los valores pasados como argumentos, el nombre y los puntos obtenidos.

```sh
class Results:

    def __init__(self, name, points):
        self.name = name
        self.points = points

    def function(self):
        return f'{self.name} has {self.points}'

cecilia = Results('Cecilia', 36)
print(cecilia.function())
Cecilia has 36
```

#### **¿Cuáles son los tres verbos de API?**

Los tres verbos API son ```GET```, ```POST``` y ```PUT```.
Los verbos de API Application Programming Interface son acciones estándares del servidor sobre los recursos que sirven para que las aplicaciones cliente puedan interactuar con él. Los verbos de API son también conocidos como métodos de petición HTTP. El Protocolo de transferencia de hipertexto HTTP es un protocolo de comunicación que sirve para transferir información en el World Wide Web.
El método ```GET``` solicita la representación de un recurso determinado. Este tipo de petición solo permiten recuperar datos del servidor.
El método ```POST``` sirve para crear un recurso. Este tipo de petición envía datos en la solicitud al servidor para crear un recurso.
El método ```PUT``` sirve para actualizar un recurso existente, es decir que sobrescribe la representación del recurso con los nuevos datos.

#### **¿Es MongoDB una base de datos SQL o NoSQL?**
   
MongoDB es una base de datos NoSQL orientada a documentos que sirve para almacenar datos de forma masiva. 
Esta base de datos NoSQL almacena los datos como colecciones y documentos en lugar de hacerlo en forma de tablas con filas y columnas como en el caso de las bases de datos SQL.
Las colecciones, similar a lo que sería una tabla, están formadas por documentos y los documentos, similar a lo que sería una fila o registro, cada uno con su id único, están formados por conjuntos de datos de pares key-value, lo que serían las columnas o campos de una tabla. La forma de construir un documento en una base de datos NoSQL es similar a cómo se crean las clases y los objetos en los lenguajes de programación como Python.
Las ventajas que aporta una base de datos NoSQL son su flexibilidad dado que no tiene estructura predeterminada, sino que se pueden añadir campos en función de la necesidad; y su escalabilidad, es decir su capacidad se puede aumentar agregando más servidores para gestionar grandes volúmenes y alta carga de tráfico de datos. 
Entre las desventajas está el hecho de que no permite relacionar documentos para hacer consultas. 
Es una tecnología joven con menos desarrolladores y administrados cualificados y falta soporte al ser una tecnología de código abierto. 

#### **¿Qué es una API?**

Una **API** (Application Programming Interfaces) es un conjunto de definiciones y protocolos que sirve para que dos aplicaciones interactúen entre sí con el objetivo de intercambiar datos.

Una API determina la forma en que deben comunicarse dos aplicaciones a través de solicitudes y respuestas. La aplicación que envía solicitudes es el cliente y la que devuelve la respuesta es el servidor. La API es el intermediario.

Por ejemplo, la base de datos del servicio público de empleo (servidor) devolverá las respuestas a las solicitudes o llamadas API enviadas desde de la aplicación móvil del servicio público de empleo(cliente) según los requisitos de la API.

Las API permiten integrar aplicaciones para intercambiar datos y automatizar procesos. Dentro de una empresa es necesario integrar los sistemas de las diferentes áreas para el trabajo conjunto, es decir, unificar las aplicaciones para que los datos se actualicen y estén disponibles en todas los sistemas. También permiten a los desarrolladores acceder a otras aplicaciones para incorporar servicios, datos y funciones externas ya creadas para construir sus propias aplicaciones sin la necesidad de empezar desde cero. 

Las API pueden ser **privadas**, cuando se usan internamente dentro de una empresa; pueden ser de **socios**, cuando se comparten con partnes empresariales o bien, pueden ser **públicas**, cuando todos tienen acceso. Esto permite que cualquiera desarrolle aplicaciones que interactuen con la API pública facilitando la innovación. 

Existen varios tipos de API:

- La **API web** es una interfaz de procesamiento de aplicaciones entre un servidor web y un navegador que utiliza protocolo ```HTTP``` para comunicarse e intercambiar datos en formato ```JSON``` (JavaScript Object Notation) o ```XML``` (Extensible Markup Language). 
- **SOAP** (Simple Object Access Protocol) es un protocolo de comunicación basado en ```XML```. Las API de SOAP son más complejas y se usan en entornos que requieren más seguridad y confiabilidad en las comunicaciones. 
- La **API de WebSocket** es una API web que usa comunicación bidireccional entre navegador y servidor e intercambia datos en formato ```JSON```. 
- **REST** (Transferencia de EStado Representacinal) es un tipo de arquitectura de software que se emplea en la creación de API web. Los clientes y los servidores intercambian datos mediante HTTP. El cliente envía solicitudes en forma de datos al servidor y este inicia funciones internas y devuelve los datos de salida al cliente. Los puntos de conexión de las **API RESTful** devuelven conjuntos predefinidos de datos. Estas API son simples y fáciles de usar.
- **GraphQL** es un lenguaje de consulta desarrollado para las API. Permite al cliente solicitar los datos específicos que necesita, reduciendo el tráfico de datos. Esto resulta en unas API más fáciles de desarrollar, más rápidas y más flexibles.


#### **¿Qué es Postman?**

Postman es una plataforma muy empleada en desarrollo web que sirve para desarrollar API. Permite gestionar el ciclo de vida de la API, desde su creación hasta su mantenimiento. Mediante esta aplicación se pueden crear, gestionar y probar las API y ofrece las siguientes herraminetas:
- Plantillas de test para REST API y End-to-end testing. 
- Posibilidad de navegar por la red de API de Postman para explorarlas.
- Creación de equipos de trabajo.
- Creación de espacios de trabajo para organizar y compartir los recursos de la API con el equipo de trabajo.
- Documentar la API usando plantillas de Postman.
- Crear redes privadas de API para el trabajo en equipo con Hub central.
- Explorar e integrar API públicas

Postman además nos permite por ejemplo crear una API RESTful que permite realizar operaciones CRUD (Create Read Update Delete) usando los métodos HTTP ```GET```, ```POST```, ```PUT```, ```PATCH``` y ```DELETE``` para operar con bases de datos. 

#### **¿Qué es el polimorfismo?**

El polimorfismo es una técnica que permite que los objetos respondan con comportamientos diferentes ante un mismo método, dependiendo de la clase del objeto. 
Hay dos formas de usar la técnica del polimorfismo, dependiendo de la necesidad. 
Si tenemos un comportamiento que se va a compartir en muchos objetos, entonces interesa usar clases derivadas de una clase padre. Aquí el método de la clase derivada sobreescribe el método de la clase padre.
Si necesitamos un comportamiento basado en una función y que no va a ser compartido, es mejor usar el polimorfismo basado en la función, con clases independientes.

#### **¿Qué es un método dunder?**

Los métodos dunders son métodos en Python que sirven para personalizar clases y objetos. 
Aportan funcionalidad y flexibilidad a las aplicaciones 
Los métodos dunders determinan el comportamiento de los objetos. Se definen y se ejecutan internamente dentro de la clase del objeto. Como son parte de la clase los métodos toman como primer argumento self haciendo referencia a uno mismo, al objeto. 
La forma de escribirlos consiste en poner dos guiones bajos delante y otros dos detrás del nombre del método.
Hay varios tipos de métodos que pueden clasificarse en función del uso. Para realizar operaciones aritméticas tenemos los métodos Suma que se escribe ```__add__```, Resta: ```__sub__```, Multiplicación: ```__mul__```, Division: ```__div__``` y ```__floordiv__```
Para operaciones de comparación tenemos los métodos Menor que, que se escribe ```__lt__```, Mayor que:```__gt__```, Igual a: ```__eq__```, Menor o igual que: ```__le__```, Mayor o igual que: ```__ge__```
Para operaciones de representación tenemos el método Str: ```__str__``` que devuelve un string legible del objeto y el método Repr: ```__repr__``` que devuelve una representación más detallada del objeto para fines de desarrollo. 
Para operar los ciclos de vida, tenemos el método Constructor: ```__init__``` que inicializa los atributos del objeto creado, el método borrado: ```__del__``` que se llama cuando se borra un objeto, el método new: ``` __new__``` sirve para crear el objeto.

Por ejemplo:
```sh
class ClassName:
    def __init__(self):
        print('Iniciando con el método __init__')

inicializar = ClassName()
```

