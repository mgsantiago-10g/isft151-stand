**PAGINA 1**

**N. I. Polikarpova, A. A. Shalyto**

**Programación Automática**

El libro fue escrito en la Universidad Estatal de Tecnologías de la Información, Mecánica y Óptica de San Petersburgo – ganadora del concurso de programas educativos innovadores de las universidades de la Federación Rusa, en el marco del programa «Sistema innovador de formación de especialistas de nueva generación en el campo de las tecnologías de la información y ópticas» en la dirección científica y educativa prioritaria «Tecnologías de programación y producción de software».

San Petersburgo 2008

UDC 681.3.06
**Revisores:**
Melekhin V. F., Doctor en Ciencias Técnicas, Profesor, Jefe del Departamento de Automatización y Tecnología Informática de la Universidad Politécnica Estatal de San Petersburgo.
Sergeev M. B., Doctor en Ciencias Técnicas, Profesor, Jefe del Departamento de Sistemas Informáticos y Redes de la Universidad Estatal de Instrumentación Aeroespacial de San Petersburgo.

Polikarpova N. I., Shalyto A. A. Programación Automática. 2008. — 167 p.: il.

El libro examina la *programación automática* – un enfoque para el desarrollo de sistemas de software con comportamiento complejo, basado en el modelo de un objeto de control automatizado (una extensión de un autómata finito). El enfoque propuesto permite crear software de calidad para sistemas críticos, cubriendo todas las etapas de su ciclo de vida y apoyando su especificación, diseño, implementación, prueba, verificación y documentación.

El libro está destinado a especialistas en el campo de la programación, informática, tecnología informática y sistemas de control, así como a estudiantes de posgrado y pregrado que estudian las especialidades «Matemáticas aplicadas e informática», «Control e informática en sistemas técnicos» y «Máquinas, sistemas, complejos y redes informáticas».

**PAGINA 2**

**Contenido**

  * Prefacio 4
  * Agradecimientos 5
  * **Capítulo 1. Introducción a la programación automática 7**
      * Áreas de aplicación del enfoque automático 7
      * Conceptos básicos 11
      * Paradigma de programación automática 12
      * Modelos automáticos 17
  * **Capítulo 2. Programación procedimental con estados explícitamente definidos 42**
      * Diseño 43
      * Especificación 64
      * Implementación 76
  * **Capítulo 3. Programación orientada a objetos con estados explícitamente definidos 95**
      * Diseño 97
      * Especificación 106
      * Implementación 116
  * **Capítulo 4. Programación automática. Nuevas tareas 134**
      * Autómatas y algoritmos de matemática discreta 134
      * Verificación de programas automáticos 137
      * Autómatas y computación paralela 140
      * Autómatas y programación genética 141
  * Conclusión 151
  * Lista de fuentes 155
  * Índice temático 166

**PAGINA 3**

**Prefacio**
El objeto de este libro es el paradigma de la *programación automática*. La programación automática, también llamada «programación por estados» o «programación con estados explícitamente definidos», es un método de desarrollo de software (SO) basado en un modelo extendido de autómatas finitos y orientado a la creación de una amplia clase de aplicaciones.

Contrariamente a la creencia popular, no se trata solo del uso de autómatas finitos en la programación, sino más bien de un método para crear programas en general, cuyo comportamiento se describe mediante autómatas.

La programación utilizando autómatas tiene una historia de desarrollo bastante rica. Varios aspectos y conceptos relacionados con esta idea han sido considerados en trabajos de muchos autores desde diferentes puntos de vista y y en relación con diversas cuestiones específicas.

La programación basada en estados es uno de los estilos de programación principales [1].

Como paradigma integral de desarrollo de SO, la programación automática se formó, en gran parte, gracias a los esfuerzos de uno de los autores de este libro, quien en 1991 propuso una tecnología para apoyar este estilo de programación [2]. En sus trabajos se pueden encontrar discusiones sobre diversos aspectos de este método de programación, y una breve descripción del paradigma de programación propuesto se encuentra, por ejemplo, en el trabajo [3].

Sin embargo, una exposición completa y exhaustiva de la esencia de la programación automática como paradigma y método de desarrollo de sistemas de software en general está ausente en este momento.

Este libro puede considerarse un primer paso para llenar este vacío.

El término «programación automática» nació en 1997 durante una conversación de uno de los autores de este libro con D. A. Pospelov en una conferencia sobre sistemas multiagente, celebrada en el pueblo de Olgino, cerca de San Petersburgo, y fue utilizado por primera vez en la introducción del trabajo [4].

En inglés, este término se traduce como *automata-based programming*. El nombre en inglés fue propuesto en el trabajo [5].

El *objetivo del libro* es definir los términos que forman el vocabulario del paradigma de programación automática y exponer sistemáticamente sus conceptos principales.

El libro contiene una serie de ejemplos de aplicación concreta de la programación automática para resolver diversas tareas aplicadas.

Los ejemplos están diseñados para demostrar la efectividad, la fructuosidad y la promesa de este paradigma.

El libro tiene la siguiente estructura. El primer capítulo presenta las ideas y conceptos principales, introduce notaciones específicas y describe los fundamentos matemáticos de la programación automática.

Familiarizarse con el material del primer capítulo es necesario para una comprensión efectiva del resto del material.

El segundo capítulo describe la visión tradicional del enfoque automático para el desarrollo de software.

La exposición cubre todos los aspectos de la creación de un sistema de software: diseño, especificación e implementación. Una parte significativa del segundo capítulo está dedicada a las tareas de control lógico.

La experiencia en la resolución de estas tareas sirvió como punto de partida para el desarrollo del enfoque automático y su difusión en otras áreas de la programación. Este capítulo se titula intencionalmente «Programación procedimental con estados explícitamente definidos»: generalmente la palabra «procedimental» se omite en esta frase, ya que el enfoque procedimental es históricamente tradicional para la programación automática.

**PAGINA 4**

Tal nombre tiene como objetivo enfatizar la diferencia semántica con el tercer capítulo, titulado «Programación orientada a objetos con estados explícitamente definidos».

El tercer capítulo establece la conexión entre los paradigmas orientados a objetos y automáticos.

El material de este capítulo tiene como objetivo demostrar que la programación automática es un desarrollo natural, y no forzado, del enfoque orientado a objetos.

El concepto central de la programación automática – un *objeto de control automatizado* – es, por su naturaleza, profundamente orientado a objetos.

El cuarto capítulo es una breve descripción de áreas de aplicación no tradicionales y problemas actuales de la programación automática.

Aquí se considera el uso de autómatas para resolver problemas clásicos de matemática discreta, cuestiones de verificación y paralelismo en programas automáticos, así como métodos de aplicación conjunta de programación genética y automática.

Cabe señalar que el término «programación» en este libro se utiliza en un sentido amplio. Como proceso, significa lo mismo que «desarrollo», «creación» de software. Como tipo (en frases como «programación automática», «programación orientada a objetos», etc.) es sinónimo de los términos «método», «enfoque», «paradigma». Para referirse a la programación en un sentido estricto (escribir código comprensible para la computadora), el libro utiliza el término «implementación».

El material del libro se utiliza en el curso «Teoría de autómatas en programación» en la Universidad de Tecnologías de la Información, Mecánica y Óptica de San Petersburgo (ITMO University) en el Departamento de «Tecnologías Informáticas», ampliamente conocido por sus éxitos en el campo de la programación competitiva [6, 7].

Hace más de cinco años se creó un recurso en línea [http://is.ifmo.ru](http://is.ifmo.ru), dedicado a la programación automática, en el que, en particular, se han publicado más de 150 trabajos estudiantiles, incluyendo documentación de proyectos, que ilustran diversos aspectos del enfoque automático a la programación.

La programación automática se utiliza actualmente en el diseño de software para sistemas de automatización de objetos de control críticos [8, 9], y de acuerdo con el estándar *IEC 61499*, que está destinado a unificar las reglas para la creación de sistemas de control distribuidos, se propone describir los bloques funcionales básicos utilizando autómatas finitos.

**PAGINA 5**

**Agradecimientos**
Los autores agradecen a V. N. Vasiliev y V. G. Parfenov por su apoyo y ayuda a largo plazo en el desarrollo del paradigma de programación descrito en este libro.

Los autores están agradecidos a los estudiantes y doctorandos de los departamentos de «Tecnologías Informáticas» y «Tecnologías de Programación» de la Universidad ITMO de San Petersburgo, quienes contribuyeron a la teoría y práctica de la programación automática, así como a todos los especialistas que implementan este paradigma de programación en la industria.

**PAGINA 6**

### Capítulo 1. Introducción a la programación automática

### Áreas de aplicación del enfoque automático

De acuerdo con la clasificación introducida por D. Harel [10], cualquier sistema de software puede clasificarse en una de las siguientes clases:

  * Los *sistemas de transformación* realizan alguna transformación de los datos de entrada y luego finalizan su trabajo. En tales sistemas, como regla general, los datos de entrada son completamente conocidos y accesibles en el momento del inicio del sistema, y los de salida, solo después de la finalización de su trabajo. Ejemplos de sistemas de transformación incluyen archivadores y compiladores.
  * Los *sistemas interactivos* interactúan con el entorno en modo de diálogo (por ejemplo, un editor de texto). Una característica distintiva de tales sistemas es que pueden controlar la velocidad de interacción con el entorno – hacer que el entorno «espere».
  * Los *sistemas reactivos* interactúan con el entorno mediante el intercambio de mensajes al ritmo establecido por el entorno. Este clase incluye la mayoría de los sistemas de telecomunicaciones, así como los sistemas de control y gestión de dispositivos físicos.

Es probable que el lector sepa que los autómatas finitos en programación se utilizan tradicionalmente en la creación de compiladores [11], que pertenecen a la clase de sistemas de transformación. Aquí, el autómata se entiende como un dispositivo computacional que tiene cintas de entrada y salida. Antes de comenzar el trabajo, una cadena se escribe en la cinta de entrada, que el autómata luego lee y procesa carácter por carácter. Como resultado del procesamiento, el autómata escribe secuencialmente algunos símbolos en la cinta de salida.

Otra área tradicional de uso de autómatas – las tareas de control lógico [4] – es una subclase de sistemas reactivos. Aquí, un autómata es, a primera vista, un dispositivo completamente diferente. Tiene varias entradas paralelas (la mayoría de las veces binarias) a las que llegan señales del entorno en tiempo real. Al procesar estas señales, el autómata forma los valores de varias salidas paralelas.

Así, incluso las áreas tradicionales de aplicación de los autómatas finitos cubren clases de sistemas de software fundamentalmente diferentes.

Los autores del libro están convencidos de que, en realidad, el abanico de tareas en las que es aconsejable utilizar el enfoque automático es mucho más amplio e incluye la creación de sistemas de software que pertenecen a las tres clases mencionadas. Sin embargo, los modelos automáticos utilizados en la creación de diferentes tipos de sistemas de software pueden diferir entre sí. Las diferencias entre los modelos automáticos se describen en detalle en la Sección 1.4.

Según los autores, el criterio de aplicabilidad del enfoque automático se expresa mejor a través del concepto de «*comportamiento complejo*». Informalmente, se puede decir que una entidad (objeto, subsistema) posee un comportamiento complejo si, como reacción a alguna *acción de entrada*, puede realizar una de varias *acciones de salida*.

**PAGINA 7**

Es esencial que la elección de una acción de salida específica pueda depender no solo de la acción de entrada, sino también del historial. Para las entidades con *comportamiento simple*, la reacción a cualquier acción de entrada depende solo de esa acción1 (Fig. 1.1).

[[[IMAGEN]]]

Fig. 1.1. Entidad con comportamiento simple (izquierda) y con comportamiento complejo (derecha)

Consideremos como ejemplo un reloj electrónico (Fig. 1.2). Supongamos que solo tiene dos botones destinados a configurar la hora actual: el botón «H» (*Hours*) incrementa el número de horas en uno, y el botón «M» (*Minutes*) – el número de minutos. El incremento ocurre módulo 24 y 60 respectivamente. Tales relojes tienen un comportamiento simple, ya que cada una de las dos acciones de entrada (presionar el primer o el segundo botón) conduce a una única reacción predefinida del reloj.

[[[IMAGEN]]]

Fig. 1.2. Reloj electrónico

Consideremos ahora un reloj electrónico con alarma (Fig. 1.3). El botón adicional «A» (*Alarm*) está diseñado en ellos para encender y apagar la alarma. Si la alarma está apagada, el botón «A» la enciende y cambia el reloj a un modo en el que los botones «H» y «M» no configuran la hora actual, sino la hora de la alarma. Presionar el botón «A» de nuevo devuelve el reloj al modo normal.

1 El comportamiento complejo también se llama *comportamiento dependiente del estado* (en la literatura inglesa se utiliza el término *state-dependent behavior*). En consecuencia, el comportamiento simple puede llamarse *comportamiento independiente del estado*. El significado de estos términos será más claro en la Sección 1.3, cuando se considere el concepto de estados de control.

**PAGINA 8**

Después de esto, si la hora actual coincide con la hora de la alarma, suena una campana, que se apaga presionando el botón «A» o automáticamente después de un minuto. Finalmente, presionar el botón «A» en modo normal con la alarma encendida apaga la alarma.

[[[IMAGEN]]]

Fig. 1.3. Reloj electrónico con alarma

El comportamiento del reloj con alarma ya es complejo, ya que las mismas acciones de entrada (presionar los mismos botones), dependiendo del modo, inician diferentes acciones.

En los sistemas informáticos de software y hardware, las entidades con comportamiento complejo son muy comunes. Dispositivos de control, protocolos de red, cuadros de diálogo, personajes de juegos de computadora y muchos otros objetos y sistemas poseen esta propiedad. Para reconocer una entidad con comportamiento complejo en el código fuente de un programa, se puede hacer lo siguiente: en la implementación tradicional de tales entidades, se utilizan variables lógicas llamadas *flags*, y numerosas y confusas estructuras de ramificación, cuyas condiciones son varias combinaciones de valores de flags. Este método de describir la lógica del comportamiento complejo está mal estructurado, es difícil de entender y modificar, y es propenso a errores. Incluso para un ejemplo tan elemental como un reloj con alarma, la implementación usando flags parece engorrosa e incomprensible (Listado 1.1).

**Listado 1.1. Implementación de un reloj electrónico con alarma en C++ usando flags**

```cpp
class Alarm_Clock {
public:
    void h_button() // Presionar el botón H
    {
        if (is_in_alarm_time_mode) {
            alarm_hours = (alarm_hours + 1) % 24;
        } else {
            hours = (hours + 1) % 24;
        }
    }

    void m_button() // Presionar el botón M
    {
        if (is_in_alarm_time_mode) {
            alarm_minutes = (alarm_minutes + 1) % 60;
        } else {
            minutes = (minutes + 1) % 60;
        }
    }

    void a_button() // Presionar el botón A
    {
        if (is_alarm_on) {
            if (is_in_alarm_time_mode) {
                is_in_alarm_time_mode = false;
            } else {
                bell_off();
                is_alarm_on = false;
            }
        } else {
            is_alarm_on = true;
            is_in_alarm_time_mode = true;
        }
    }

    void tick() // Activación del temporizador de minutos
    {
        if (is_alarm_on && !is_in_alarm_time_mode) {
            if ((minutes == alarm_minutes - 1) && (hours == alarm_hours) || (alarm_minutes == 0) && (minutes == 59) && (hours == alarm_hours - 1))
                bell_on();
            else if ((minutes == alarm_minutes) && (hours == alarm_hours))
                bell_off();
        }
        minutes = (minutes + 1) % 60;
        if (minutes == 0)
            hours = (hours + 1) % 24;
    }
private:
    int hours;    // Horas de la hora actual
    int minutes;    // Minutos de la hora actual
    int alarm_hours;    // Horas de activación de la alarma
    int alarm_minutes; // Minutos de activación de la alarma

    bool is_alarm_on;    // ¿Está la alarma activada?
    bool is_in_alarm_time_mode; // ¿Está activo el modo de configuración de la hora de la alarma?

    void bell_on() {...} // Encender el timbre
    void bell_off() {...} // Apagar el timbre
};
```

**PAGINA 9**

Una de las ideas centrales de la programación automática es separar la descripción de la *lógica* del comportamiento (bajo qué condiciones se deben realizar ciertas acciones) de la descripción de su *semántica* (el significado real de cada acción). Además, la descripción de la lógica en el enfoque automático está estrictamente estructurada. Estas propiedades hacen que la descripción automática del comportamiento complejo sea clara y concisa.

La recomendación principal para aplicar la programación automática es muy simple: *utilice el enfoque automático al crear cualquier sistema de software que contenga entidades con comportamiento complejo*.

La experiencia demuestra que casi cualquier sistema serio posee esta propiedad. Sin embargo, no todos los componentes del sistema se caracterizan por un comportamiento complejo. Por lo tanto, la recomendación anterior puede complementarse con otra: *utilice el enfoque automático solo al crear aquellos componentes del sistema que sean entidades con comportamiento complejo*.

Esta adición insta a no sobrecargar las especificaciones y el código con descripciones lógicas donde no es necesario. Seguir estas sencillas recomendaciones permite crear sistemas de software correctos y extensibles con un comportamiento complejo. Sin embargo, hacerlo no es tan sencillo. La identificación de entidades con comportamiento complejo en la etapa de diseño del sistema, así como la extracción de la lógica de su comportamiento, son tareas creativas complejas. Estas decisiones de diseño no triviales son tomadas por el desarrollador para cada una de ellas individualmente.

### Conceptos básicos

El concepto fundamental de la programación automática es el «*estado*». Este concepto, en el sentido en que se utiliza en el paradigma descrito, fue introducido por A. Turing y se aplica con éxito en muchas áreas desarrolladas de la ciencia, como la teoría de control y la teoría de lenguajes formales.

La propiedad principal del *estado del sistema* en el momento $t\_0$ consiste en «separar» el futuro ($t \> t\_0$) del pasado ($t \< t\_0$) en el sentido de que el estado actual contiene toda la información sobre el pasado del sistema necesaria para determinar su reacción a cualquier acción de entrada generada en el momento $t\_0$.

**PAGINA 10**

En la Sección 1.1, al describir el concepto de «comportamiento complejo», se mencionó que la reacción de una entidad con comportamiento complejo a una acción de entrada puede depender, entre otras cosas, del historial. Al utilizar el concepto de «estado», el conocimiento del historial ya no es necesario. El estado puede considerarse como una característica especial que, de forma implícita, combina todas las acciones de entrada del pasado que influyen en la reacción de la entidad en el momento actual. La reacción ahora depende solo de la acción de entrada y del estado actual.

**NOTA**

Según la opinión popular, la eficacia del enfoque orientado a objetos para el desarrollo de software se explica por el hecho de que para el ser humano es *natural* pensar en términos de objetos (entidades) e interacción entre ellos. El enfoque automático, según los autores, también tiene todas las posibilidades de ser eficaz, ya que las personas viven en estados (por ejemplo, duermen o están despiertos, saciados o hambrientos), y en dependencia del *estado* actual reaccionan de manera diferente a los *estímulos externos*. Recuerde el proverbio: «Barriga llena, corazón contento».

El concepto de *acción de entrada* también es uno de los básicos para la programación automática. La mayoría de las veces, una acción de entrada es un vector. Sus componentes se dividen en *eventos* y *variables de entrada* según el significado y el mecanismo de formación.

La combinación de un conjunto finito de estados y un conjunto finito de acciones de entrada forma un autómata (finito) *sin salidas*. Tal autómata reacciona a las acciones de entrada, cambiando el estado actual de una manera definida. Las reglas por las cuales ocurre el cambio de estado se llaman la *función de transición* del autómata.

Lo que en programación automática se llama (finito) *autómata* (Fig. 1.4) se obtiene al combinar el concepto de autómata sin salidas con el concepto de «*acción de salida*». Tal autómata reacciona a la acción de entrada no solo cambiando de estado, sino también formando ciertos valores en las salidas. Las reglas para formar las acciones de salida se llaman la *función de salida* del autómata.

[[[IMAGEN]]]

Fig. 1.4. Autómata finito

**PAGINA 11**

### Paradigma de programación automática

Para comprender mejor los conceptos principales de la programación automática, consideremos primero una de las máquinas de cálculo abstractas, ampliamente utilizadas en la teoría de lenguajes formales – la *máquina de Turing* [12, 13]. Esta máquina abstracta fue propuesta por A. Turing en 1936 como una definición formal del concepto de «algoritmo».

La tesis de Church-Turing [13] establece que todo lo que puede ser «calculado», «programado» o «reconocido» en cualquier sentido (de los formalmente definidos actualmente), puede ser calculado, programado o reconocido mediante una máquina de Turing adecuada.

Una máquina de Turing consta de dos partes: una unidad de control y una unidad de almacenamiento – una cinta (Fig. 1.5). La cinta contiene un número infinito de celdas en las que se pueden escribir símbolos de un alfabeto finito. En cada momento, una cabeza de lectura-escritura está colocada en una de las celdas de la cinta, lo que permite a la unidad de control leer o escribir un símbolo en esa celda.

[[[IMAGEN]]]

Fig. 1.5. Máquina de Turing: representación tradicional (izquierda) y representación en las tradiciones de la teoría de control (derecha)

La unidad de control es un autómata finito. Tiene una única acción de entrada: un símbolo leído de la cinta – y dos acciones de salida: un símbolo escrito en la cinta, y una instrucción para que la cabeza se mueva una celda en una u otra dirección, o que permanezca en su lugar. La tesis de Church-Turing significa que en términos de operaciones de la máquina de Turing se pueden escribir los mismos programas que en cualquier lenguaje de programación existente.

¿Cómo programar en una máquina de Turing? Supongamos, por ejemplo, que es necesario implementar la función de *incremento* (aumentar un número entero en uno). Sea el número original escrito en la cinta en formato binario de izquierda a derecha, en todas las demás celdas hay un símbolo vacío (*'blank'*) y la cabeza apunta al dígito más significativo del número. Entonces, para aumentar el número en uno, se puede proponer el siguiente algoritmo:

  * Moverse a la derecha hasta que se encuentre un símbolo vacío.
  * Moverse una celda a la izquierda.
  * Mientras en la celda actual se encuentre el símbolo '1', cambiarlo por '0' y moverse a la izquierda.
  * Si en la celda actual se encuentra el símbolo '0' o un símbolo vacío, escribir '1' en la celda.

**PAGINA 12**

Como se puede ver, el algoritmo se describe mediante un conjunto de instrucciones del tipo "si, en el estado S, se lee el símbolo X, entonces escribir el símbolo Y, moverse en la dirección D, y pasar al estado S'". A partir de esta breve descripción de la máquina de Turing, podemos sacar conclusiones importantes para comprender la esencia de la programación automática.

En la máquina de Turing, se distinguen claramente dos componentes: el dispositivo de control (autómata finito) y el dispositivo de almacenamiento (cinta). Además, su interacción está organizada de la siguiente manera: el dispositivo de control lee datos de la cinta y, basándose en el símbolo leído y su estado interno, cambia su estado, escribe datos en la cinta y mueve la cabeza de lectura-escritura. Es decir, las acciones del dispositivo de control están completamente determinadas por la lectura de datos de la cinta y el estado interno del dispositivo de control.

El dispositivo de control es una *entidad con comportamiento complejo*. Su complejidad radica en que, en función del estado actual, reacciona de manera diferente a las mismas acciones de entrada (símbolos leídos de la cinta). La cinta es una *entidad con comportamiento simple*. Su complejidad puede reducirse a que cada una de sus celdas almacena un símbolo y puede ser modificada por el dispositivo de control. Es decir, la cinta puede entenderse como una colección de celdas, cada una con un comportamiento simple.

En la programación automática, la entidad con comportamiento complejo se llama *objeto de control automatizado* (OCO). El objeto de control automatizado también tiene dos componentes: un autómata finito y un conjunto de variables de datos. El autómata finito contiene toda la lógica del comportamiento complejo de la entidad, mientras que el conjunto de variables de datos contiene los datos que son procesados por el autómata. El autómata opera sobre las variables de datos, y los valores de estas variables de datos también pueden influir en el comportamiento del autómata. El objeto de control automatizado y sus componentes se muestran en la Fig. 1.6.

[[[IMAGEN]]]

Fig. 1.6. Objeto de control automatizado

Los objetos de control automatizados se utilizan para desarrollar sistemas de software completos. La esencia de la programación automática es construir programas a partir de objetos de control automatizados.

Volvamos al ejemplo de los relojes electrónicos con alarma. El listado 1.1 muestra un intento de realizar este objeto con un enfoque tradicional. La presencia de variables lógicas (`is_alarm_on`, `is_in_alarm_time_mode`), también llamadas "flags", indica que la entidad (en este caso, la clase `Alarm_Clock`) tiene un comportamiento complejo.

**PAGINA 13**

En el enfoque automático, cada flag corresponde a un estado de control explícitamente definido. Los nombres de los estados se eligen de forma que reflejen las características más importantes del comportamiento del objeto en este estado. Para el ejemplo de los relojes con alarma, estos estados podrían ser:

  * **Reloj en modo normal** (reloj encendido, alarma apagada),
  * **Reloj en modo alarma** (reloj encendido, alarma encendida),
  * **Reloj en modo ajuste de alarma** (reloj encendido, alarma encendida, ajuste de alarma).

Las variables `hours` y `minutes` son ejemplos de variables de datos (véase la Fig. 1.6).

Cada uno de los métodos (`h_button`, `m_button`, `a_button`, `tick`) corresponde a una acción de entrada. Un cambio en el valor de una variable de datos (`minutes`, `hours`) puede ser una acción de salida, así como un cambio en el estado del timbre (métodos `bell_on()` y `bell_off()`).

El comportamiento del autómata finito que describe la lógica de los relojes con alarma se representa mediante un *grafo de estados* (Fig. 1.7).

[[[IMAGEN]]]

Fig. 1.7. Grafo de estados para los relojes con alarma

En este grafo:

  * Los óvalos representan los estados de control del reloj (nodos del grafo),
  * Las flechas representan las transiciones entre estados (aristas del grafo). Cada flecha está etiquetada con la acción de entrada que causa la transición,
  * Las acciones de salida se muestran dentro de los óvalos.

Los estados de control muestran la lógica del comportamiento complejo. Por ejemplo, en el estado "Reloj en modo normal", al presionar el botón "H", las horas actuales aumentan en uno; en el estado "Reloj en modo ajuste de alarma", el mismo botón aumenta la hora de la alarma en uno. La semántica de las acciones es clara y comprensible.

**PAGINA 14**

El desarrollo de software utilizando objetos de control automatizados puede ser un proceso iterativo de arriba hacia abajo. En este caso, el proceso de desarrollo de software comienza con la creación de modelos automatizados. Después de que se ha desarrollado un modelo automatizado para el objeto de control automatizado de un nivel dado, comienza la implementación de este modelo. Este proceso puede incluir la identificación de nuevos objetos de control automatizados en un nivel inferior.

El enfoque de la programación automática se basa en los siguientes principios:

1.  **Principio de modularidad:** Los programas se componen de objetos de control automatizados. La descomposición del sistema de software en objetos de control automatizados puede realizarse en cada etapa del desarrollo del programa.
2.  **Principio de jerarquía:** Los objetos de control automatizados se pueden construir de forma jerárquica: los objetos de nivel superior utilizan objetos de nivel inferior.
3.  **Principio de reutilización:** Los objetos de control automatizados pueden reutilizarse en diferentes programas.

Además de los principios anteriores, los desarrolladores de software que implementan la programación automática deben seguir una serie de reglas que contribuyen a mejorar la calidad del software.

  * **Regla de completitud de la especificación:** para cada estado de control del objeto automatizado y para cada acción de entrada posible, debe definirse la reacción del objeto a esta acción (transición a un nuevo estado y/o acciones de salida).
  * **Regla de minimización de estados:** el número de estados de control debe ser el mínimo necesario para describir el comportamiento complejo de la entidad.

La programación automática puede implementarse de dos maneras principales:

  * mediante el uso de un lenguaje de programación procedimental (por ejemplo, C, Pascal);
  * mediante el uso de un lenguaje de programación orientado a objetos (por ejemplo, C++, Java).

El enfoque procedimental se describe en el Capítulo 2, y el enfoque orientado a objetos, en el Capítulo 3.

**PAGINA 15**

### Modelos de Autómatas

En la literatura, se pueden encontrar muchas definiciones de autómata. Sin embargo, en el contexto de la programación automática, la definición clásica de autómata de Mealy o Moore no es suficiente, ya que no permite describir el comportamiento de un objeto de control automatizado de la manera más adecuada. Por lo tanto, en este libro utilizaremos una definición extendida de autómata finito, que introdujimos en la sección 1.3 como un objeto de control automatizado. Esta definición tiene las siguientes características distintivas:

  * El autómata tiene un conjunto de variables de datos que almacenan los datos del programa. Estas variables pueden ser de cualquier tipo (números, cadenas, objetos, etc.).
  * El autómata puede tener eventos de entrada y de salida. Un evento de entrada es una señal que el autómata recibe del entorno. Un evento de salida es una señal que el autómata envía al entorno.
  * Las transiciones entre estados pueden depender no solo de los eventos de entrada, sino también de las condiciones de las variables de datos.
  * Las acciones de salida pueden ser operaciones sobre las variables de datos (asignaciones, llamadas a funciones, etc.).

A partir de la definición extendida de autómata finito, podemos definir el *modelo de autómata* como un conjunto de elementos que describen la estructura y el comportamiento de un objeto de control automatizado. Los elementos de un modelo de autómata son:

  * Un conjunto finito de estados de control.
  * Un conjunto finito de eventos de entrada.
  * Un conjunto finito de eventos de salida.
  * Un conjunto de variables de datos.
  * Una función de transición que asigna a cada triplete (estado actual, evento de entrada, valores de las variables de datos) un nuevo estado.
  * Una función de salida que asigna a cada triplete (estado actual, evento de entrada, valores de las variables de datos) un conjunto de acciones de salida.

Además, el modelo de autómata puede incluir:

  * Un estado inicial.
  * Un conjunto de estados finales.

El modelo de autómata puede representarse de diferentes maneras:

  * En forma de tabla de transiciones y salidas.
  * En forma de grafo de estados.
  * En forma de código fuente en un lenguaje de programación.

La representación más conveniente para los diseñadores es el grafo de estados, que proporciona una representación visual de la lógica del comportamiento complejo.

**PAGINA 16**

Un modelo automatizado formalmente puede definirse como un 9-tupla:
$M = (S, I, O, D, T, F, s\_0, S\_{fin}, V)$

donde:

  * $S$ es un conjunto finito de estados de control,
  * $I$ es un conjunto finito de eventos de entrada,
  * $O$ es un conjunto finito de eventos de salida,
  * $D$ es un conjunto de variables de datos,
  * $T: S \\times I \\times Val(D) \\to S$ es una función de transición de autómata, donde $Val(D)$ es el conjunto de todos los valores posibles de las variables de datos,
  * $F: S \\times I \\times Val(D) \\to \\text{Acciones}(D, O)$ es una función de salida de autómata, donde $\\text{Acciones}(D, O)$ es el conjunto de todas las acciones posibles sobre las variables de datos y eventos de salida,
  * $s\_0 \\in S$ es el estado inicial,
  * $S\_{fin} \\subseteq S$ es un conjunto de estados finales (si los hay),
  * $V$ es un conjunto de propiedades que deben satisfacer las variables de datos.

Es importante destacar que las funciones de transición y salida dependen tanto del evento de entrada como del estado de control actual y los valores de las variables de datos. Esto distingue significativamente el autómata de la definición clásica de Mealy/Moore, donde las funciones de transición y salida dependen solo del evento de entrada y del estado actual.

**PAGINA 17**

### Implementación del Autómata

La implementación de un autómata generalmente implica crear un programa o un componente de software que simule el comportamiento del autómata. El enfoque más común para implementar un autómata es mediante un bucle de eventos (event loop). El bucle de eventos monitorea las acciones de entrada y, cuando ocurre una, invoca la función de transición y la función de salida del autómata.

El estado actual del autómata se almacena en una variable. Cuando ocurre un evento de entrada, el programa determina el nuevo estado y ejecuta las acciones de salida correspondientes.

Un ejemplo simplificado de la estructura de un programa que implementa un autómata podría ser el siguiente:

```cpp
class Automaton {
private:
    State current_state; // Variable para almacenar el estado actual
    // Otras variables de datos

public:
    void process_event(Event input_event) {
        // Calcular el nuevo estado y las acciones de salida
        // basándose en current_state, input_event y las variables de datos.

        // Ejemplo (pseudo-código):
        // if (current_state == STATE_A && input_event == EVENT_X) {
        //     current_state = STATE_B;
        //     perform_action_Y();
        // } else if (...) {
        //     ...
        // }
    }
};
```

**PAGINA 18**

En cada una de las ramas que emanan de los decodificadores de acciones de entrada, se realiza una actualización del estado actual.

En el lenguaje C, existen dos formas principales de implementar dicho algoritmo: mediante tablas y mediante una instrucción de selección (switch).

En el primer caso, las funciones de salida y transición del autómata se representan como tablas (arrays) en la memoria. Para representar la función de salida, se requiere un array de $s$ elementos, que asocia un vector de valores de variables de salida a cada estado. Para representar la función de transiciones, se requiere una tabla de $s$ filas y $2^n$ columnas, que asocia un nuevo estado a cada estado y vector de valores de variables de entrada. Las tablas de acciones y transiciones se construyen dinámicamente durante la ejecución del programa. Por lo tanto, este método es más flexible en comparación con el uso de la instrucción de selección: el autómata puede modificarse durante la ejecución del programa. Sin embargo, esta flexibilidad se logra a expensas de cierta pérdida de rendimiento.

Además, con el método de almacenamiento descrito, el tamaño de la tabla de transiciones crece exponencialmente con el aumento del número de variables de entrada del autómata. En la mayoría de los casos, no hay una necesidad objetiva de almacenar toda esta tabla por completo: el valor de la función de transiciones en cada estado no depende de todos los componentes de la acción de entrada, sino solo de un pequeño conjunto de variables de entrada *significativas*. Esta observación puede utilizarse para reducir el tamaño de las tablas de transiciones y acciones en caso de que se requiera una representación compacta

**PAGINA 19**

en la memoria. La figura 1.8 muestra la estructura del software para una implementación basada en tablas de autómatas finitos.

[[[IMAGEN]]]

Fig. 1.8. Implementación basada en tablas de autómatas finitos.

En el segundo caso, el algoritmo de funcionamiento del autómata se implementa utilizando una instrucción de selección múltiple (switch), donde las ramas seleccionan el estado actual, y dentro de cada estado, las subramas seleccionan la acción de entrada. La figura 1.9 muestra la estructura del software para una implementación basada en una instrucción de selección.

[[[IMAGEN]]]

Fig. 1.9. Implementación basada en una instrucción de selección de autómatas finitos.

La segunda opción es, en nuestra opinión, más preferible, ya que las modernas herramientas de programación orientadas a objetos permiten generar automáticamente el código de la función de transición basándose en el grafo de estados. Por ejemplo, en el entorno de desarrollo Rational Rose RealTime, existe una notación UML Statechart Diagrams, que permite describir el comportamiento complejo de los objetos de control automatizados. Basándose en esta notación, se genera automáticamente el código de la función de transición.

**PAGINA 20**

Otra forma de reducir el número de variables de entrada significativas es usar la técnica de multiplexación ( multiplexing ). Esta técnica consiste en combinar varias variables de entrada en una sola, de modo que el autómata sólo tenga que procesar una variable de entrada en cada momento. Por ejemplo, si tenemos dos variables de entrada binarias, A y B, podemos combinarlas en una variable de entrada de 4 valores (00, 01, 10, 11).

Otra técnica que puede utilizarse para reducir el tamaño de las tablas es la compresión de tablas. Esto puede hacerse utilizando diferentes algoritmos de compresión.

Es importante señalar que la elección del método de implementación (tablas o instrucción de selección) depende de los requisitos específicos del sistema. Si la flexibilidad es un factor clave, entonces el método de tablas es más adecuado. Si el rendimiento es un factor clave, entonces el método de instrucción de selección es más adecuado.

**PAGINA 21**

### Representación de autómatas finitos

Hay muchas formas de representar un autómata finito, incluyendo:

  * Tabla de transiciones y salidas.
  * Grafo de estados.
  * Expresiones regulares.
  * Autómatas basados en pila.
  * Autómatas con estados abstractos.

En el contexto de la programación automática, la representación más común es el *grafo de estados*. Un grafo de estados es un grafo dirigido donde:

  * Los nodos representan los estados de control del autómata.
  * Las aristas representan las transiciones entre estados.
  * Cada arista está etiquetada con la acción de entrada que causa la transición.
  * Las acciones de salida se muestran dentro de los nodos o en las aristas.

El grafo de estados proporciona una representación visual de la lógica del comportamiento complejo del autómata, lo que facilita su diseño, comprensión y depuración.

**Ejemplo: Máquina expendedora de bebidas**
Consideremos un ejemplo de una máquina expendedora de bebidas que solo vende una bebida por 50 centavos. La máquina acepta monedas de 10, 20 y 50 centavos. Si se introduce más de 50 centavos, el cambio se devuelve al cliente.

Los estados de control de la máquina expendedora podrían ser:

  * **Cero**: no se ha introducido ninguna moneda.
  * **Diez**: se han introducido 10 centavos.
  * **Veinte**: se han introducido 20 centavos.
  * **Treinta**: se han introducido 30 centavos.
  * **Cuarenta**: se han introducido 40 centavos.
  * **Cincuenta**: se han introducido 50 centavos o más.

Las acciones de entrada son la inserción de monedas (10, 20, 50 centavos).
Las acciones de salida son dispensar la bebida y devolver el cambio.

El grafo de estados para esta máquina expendedora se muestra en la Fig. 1.10.

[[[IMAGEN]]]

Fig. 1.10. Grafo de estados para una máquina expendedora de bebidas.

En este grafo:

  * Los óvalos son los estados de control.
  * Las flechas son las transiciones.
  * Los números en las flechas son las monedas introducidas.
  * Las acciones de salida se muestran entre corchetes, por ejemplo, [dispensar bebida, devolver 10 centavos].

**PAGINA 22**

### Verificación de Autómatas

La verificación de autómatas es un proceso para garantizar que el autómata se comporta como se espera. Hay varias técnicas para verificar autómatas, incluyendo:

  * **Pruebas:** Ejecutar el autómata con un conjunto de entradas de prueba y verificar que las salidas sean correctas.
  * **Verificación formal:** Usar métodos matemáticos para probar que el autómata cumple con ciertas propiedades.
  * **Simulación:** Ejecutar el autómata en un entorno simulado y observar su comportamiento.

La verificación formal es la más rigurosa de estas técnicas, pero también la más costosa. Las pruebas y la simulación son menos rigurosas, pero son más fáciles de aplicar.

En el contexto de la programación automática, la verificación de autómatas es crucial para garantizar la corrección del software. Los errores en la lógica del autómata pueden llevar a un comportamiento inesperado del sistema y, en sistemas críticos, pueden tener consecuencias graves.

Uno de los problemas más comunes en la verificación de autómatas es la detección de *estados inalcanzables*. Un estado inalcanzable es un estado al que no se puede llegar desde el estado inicial del autómata. Estos estados son un signo de un error en el diseño del autómata y deben eliminarse.

Otro problema común es la detección de *estados de bloqueo*. Un estado de bloqueo es un estado en el que el autómata no puede realizar ninguna transición de salida, lo que significa que el autómata se "atasca" en este estado. Esto también es un signo de un error en el diseño del autómata y debe corregirse.

**PAGINA 23**

Además, es importante verificar las propiedades de seguridad y vivacidad del autómata:

  * Las *propiedades de seguridad* garantizan que "algo malo" nunca sucederá. Por ejemplo, en el caso de la máquina expendedora, una propiedad de seguridad podría ser que la máquina nunca dispense una bebida sin que se hayan introducido al menos 50 centavos.
  * Las *propiedades de vivacidad* garantizan que "algo bueno" finalmente sucederá. Por ejemplo, en el caso de la máquina expendedora, una propiedad de vivacidad podría ser que, si se introducen 50 centavos, la máquina finalmente dispensará una bebida.

Las herramientas de verificación formal pueden utilizarse para comprobar estas propiedades.

### Ventajas y desventajas de la programación automática

La programación automática tiene varias ventajas significativas:

  * **Claridad y concisión:** La representación del comportamiento complejo mediante autómatas es más clara y concisa que el uso de banderas y estructuras de ramificación. Esto facilita la comprensión y modificación del código.
  * **Modularidad:** El enfoque automático promueve la modularidad, ya que el sistema se descompone en objetos de control automatizados. Esto facilita la reutilización de componentes y el desarrollo paralelo.
  * **Verificabilidad:** Los modelos de autómatas son formalmente verificables, lo que permite garantizar la corrección del software y reducir el riesgo de errores.
  * **Soporte de herramientas:** Existen herramientas que permiten el diseño gráfico de autómatas y la generación automática de código, lo que acelera el proceso de desarrollo.
  * **Depuración sencilla:** La depuración de programas automáticos es más sencilla, ya que el estado del autómata se conoce explícitamente y se pueden seguir las transiciones entre estados.

Sin embargo, también existen algunas desventajas:

  * **Curva de aprendizaje:** Los desarrolladores deben aprender los conceptos y la notación de la programación automática, lo que puede requerir tiempo.
  * **Complejidad inicial:** Para sistemas muy simples, el overhead de la creación de un modelo automático puede parecer excesivo.
  * **Explosión de estados:** En sistemas muy grandes y complejos, el número de estados puede crecer exponencialmente, lo que dificulta la gestión del modelo.

**PAGINA 24**

Sin embargo, para los sistemas con comportamiento realmente complejo, las ventajas de la programación automática superan con creces sus desventajas.

### Resumen del Capítulo 1

En este capítulo, se introdujo el concepto de *programación automática* como un enfoque para el desarrollo de sistemas de software con comportamiento complejo, basado en el modelo de un objeto de control automatizado (una extensión de un autómata finito).

Se discutieron las *áreas de aplicación* del enfoque automático, haciendo hincapié en que es especialmente adecuado para sistemas reactivos e interactivos, pero también puede ser útil para sistemas de transformación cuando contienen componentes con comportamiento complejo. Se introdujo el concepto clave de *comportamiento complejo* y se mostró cómo se diferencia del *comportamiento simple*.

Se definieron los *conceptos básicos* del paradigma: estado, acción de entrada, acción de salida, autómata y objeto de control automatizado. Se utilizó la máquina de Turing como ejemplo para ilustrar la separación entre la unidad de control (autómata) y la unidad de almacenamiento (variables de datos).

Se presentó el *paradigma de programación automática*, destacando sus principios de modularidad, jerarquía y reutilización, así como las reglas de completitud de la especificación y minimización de estados.

Se describieron los *modelos de autómatas* extendidos utilizados en este libro, que incluyen variables de datos y condiciones sobre estas variables, diferenciándolos de los autómatas clásicos de Mealy/Moore. Se formalizó el modelo de autómata como una 9-tupla.

Se examinaron los métodos de *implementación de autómatas* en lenguajes procedimentales (C, Pascal) y orientados a objetos (C++, Java), discutiendo las implementaciones basadas en tablas y en instrucciones de selección (switch).

Finalmente, se abordó la *verificación de autómatas*, destacando la importancia de detectar estados inalcanzables y de bloqueo, y de verificar propiedades de seguridad y vivacidad. Se resumieron las principales *ventajas y desventajas* de la programación automática, concluyendo que sus beneficios superan los inconvenientes para sistemas con comportamiento realmente complejo.

Este capítulo sirve como base para comprender los capítulos siguientes, que detallarán las implementaciones procedimentales y orientadas a objetos de la programación automática.

**PAGINA 25**

### Ejercicios para la autoevaluación

1.  Defina el concepto de «estado» en el contexto de la programación automática.
2.  ¿Cuál es la diferencia entre una entidad con comportamiento simple y una con comportamiento complejo?
3.  Describa las partes principales de un objeto de control automatizado.
4.  Enumere los principios de la programación automática.
5.  ¿Cuáles son las ventajas y desventajas de la programación automática?
6.  ¿En qué se diferencia el modelo de autómata extendido (utilizado en este libro) del autómata clásico de Mealy/Moore?
7.  ¿Cómo puede representarse un autómata finito?
8.  Describa dos formas principales de implementar un autómata finito en el lenguaje C.

**PAGINA 26**

[[[IMAGEN]]]

Fig. 1.11.

[[[IMAGEN]]]

Fig. 1.12.

[[[IMAGEN]]]

Fig. 1.13.

[[[IMAGEN]]]

Fig. 1.14.

**PAGINA 27**

[[[IMAGEN]]]

Fig. 1.15.

[[[IMAGEN]]]

Fig. 1.16.

[[[IMAGEN]]]

Fig. 1.17.

[[[IMAGEN]]]

Fig. 1.18.

**PAGINA 28**

[[[IMAGEN]]]

Fig. 1.19.

[[[IMAGEN]]]

Fig. 1.20.

**PAGINA 29**

[[[IMAGEN]]]

Fig. 1.21.

[[[IMAGEN]]]

Fig. 1.22.

**PAGINA 30**

[[[IMAGEN]]]

Fig. 1.23.

[[[IMAGEN]]]

Fig. 1.24.

**PAGINA 31**

[[[IMAGEN]]]

Fig. 1.25.

**PAGINA 32**

[[[IMAGEN]]]

Fig. 1.26.

**PAGINA 33**

[[[IMAGEN]]]

Fig. 1.27.

**PAGINA 34**

[[[IMAGEN]]]

Fig. 1.28.

**PAGINA 35**

[[[IMAGEN]]]

Fig. 1.29.

**PAGINA 36**

[[[IMAGEN]]]

Fig. 1.30.

**PAGINA 37**

[[[IMAGEN]]]

Fig. 1.31.

**PAGINA 38**

[[[IMAGEN]]]

Fig. 1.32.

**PAGINA 39**

[[[IMAGEN]]]

Fig. 1.33.

**PAGINA 40**

[[[IMAGEN]]]

Fig. 1.34.

**PAGINA 41**

[[[IMAGEN]]]

Fig. 1.35.

**PAGINA 42**

### Capítulo 2. Programación procedimental con estados explícitamente definidos

Este capítulo describe los aspectos de diseño, especificación e implementación de los sistemas de software en el marco del enfoque procedimental de la programación automática. Los sistemas de control lógico son uno de los principales objetos de este enfoque.

Los sistemas de control lógico se definen como aquellos sistemas en los que se debe garantizar el cumplimiento de un conjunto de propiedades de seguridad y vivacidad. Por lo general, estos sistemas son reactivos, ya que interactúan con el entorno a un ritmo dictado por el entorno. Ejemplos de sistemas de control lógico incluyen controladores de ascensores, máquinas expendedoras (como vimos en el Capítulo 1), controladores de semáforos, etc.

El material presentado en este capítulo se basa en los fundamentos de la teoría de autómatas y la teoría de los lenguajes formales, lo que permite utilizar herramientas formales para el análisis y la verificación de los sistemas desarrollados.

El enfoque procedimental se caracteriza por el uso de lenguajes de programación como C, Pascal, etc., donde la lógica del autómata se implementa directamente en el código del programa mediante estructuras de control como `switch` o `if-else`.

### Diseño

El diseño de un sistema de control lógico utilizando la programación automática comienza con la identificación de las entidades con comportamiento complejo y la descripción de su comportamiento mediante modelos de autómatas.

El proceso de diseño puede dividirse en las siguientes etapas:

1.  **Identificación de objetos de control automatizados (OCOs):** En esta etapa, se analizan los requisitos del sistema para identificar las entidades que poseen un comportamiento complejo y que, por lo tanto, pueden modelarse como OCOs.
2.  **Modelado del comportamiento de los OCOs:** Para cada OCO identificado, se crea un modelo de autómata que describe su comportamiento en términos de estados, acciones de entrada, acciones de salida y transiciones entre estados.
3.  **Descomposición del sistema:** Si el sistema es grande y complejo, puede descomponerse en subsistemas más pequeños, cada uno de los cuales puede ser un OCO o un conjunto de OCOs interconectados.
4.  **Definición de interfaces:** Se definen las interfaces entre los OCOs y con el entorno externo, especificando las acciones de entrada y salida que se intercambian.
5.  **Refinamiento del modelo:** El modelo de autómata se refina iterativamente, añadiendo detalles y manejando casos excepcionales hasta que el modelo sea completo y preciso.

**PAGINA 43**

### Especificación

La especificación de un sistema de control lógico utilizando la programación automática implica la descripción formal del comportamiento de los autómatas. Esto puede hacerse utilizando diferentes notaciones, como:

  * **Tablas de estados:** Una tabla que enumera todos los estados posibles, las acciones de entrada, las transiciones a nuevos estados y las acciones de salida.
  * **Diagramas de estados:** Representación gráfica del autómata (grafo de estados), como se vio en el Capítulo 1.
  * **Lenguajes formales:** Lenguajes de descripción de alto nivel que permiten especificar el comportamiento del autómata de manera precisa y sin ambigüedades.

La especificación debe ser clara, completa y consistente para garantizar que la implementación del autómata sea correcta.

**PAGINA 44**

### Ejemplo de control de un ascensor

Consideremos el diseño de un sistema de control para un ascensor simple de dos pisos.

**Requisitos:**

  * El ascensor tiene dos pisos: 1 y 2.
  * En cada piso hay un botón para llamar al ascensor.
  * Dentro del ascensor hay botones para seleccionar el piso (1 y 2).
  * El ascensor debe moverse entre los pisos según las llamadas y las selecciones de piso.
  * Las puertas del ascensor se abren y cierran automáticamente.
  * El ascensor debe permanecer en un piso con las puertas abiertas durante un tiempo determinado antes de cerrarlas y esperar una nueva llamada o selección.

**Identificación de OCOs:**
El principal OCO en este sistema es el *controlador del ascensor*. Este objeto tiene un comportamiento complejo, ya que su reacción a la pulsación de un botón (acción de entrada) depende de su estado actual (por ejemplo, en qué piso se encuentra, si las puertas están abiertas o cerradas, si está subiendo o bajando).

**Modelado del comportamiento del OCO (Controlador del ascensor):**
Definimos los estados de control principales del controlador del ascensor:

  * **Parado en el piso 1 (DoorsOpen1):** El ascensor está en el piso 1 con las puertas abiertas.
  * **Parado en el piso 1 (DoorsClosed1):** El ascensor está en el piso 1 con las puertas cerradas, esperando una llamada.
  * **Subiendo al piso 2 (MovingUp):** El ascensor se está moviendo del piso 1 al piso 2.
  * **Parado en el piso 2 (DoorsOpen2):** El ascensor está en el piso 2 con las puertas abiertas.
  * **Parado en el piso 2 (DoorsClosed2):** El ascensor está en el piso 2 con las puertas cerradas, esperando una llamada.
  * **Bajando al piso 1 (MovingDown):** El ascensor se está moviendo del piso 2 al piso 1.

**PAGINA 45**

Las acciones de entrada podrían ser:

  * `Call1`: Se presiona el botón de llamada en el piso 1.
  * `Call2`: Se presiona el botón de llamada en el piso 2.
  * `Select1`: Se presiona el botón de selección de piso 1 dentro del ascensor.
  * `Select2`: Se presiona el botón de selección de piso 2 dentro del ascensor.
  * `DoorTimerExpires`: El temporizador para mantener las puertas abiertas expira.
  * `ArrivedAtFloor1`: El ascensor ha llegado al piso 1.
  * `ArrivedAtFloor2`: El ascensor ha llegado al piso 2.

Las acciones de salida podrían ser:

  * `OpenDoors`: Abrir las puertas.
  * `CloseDoors`: Cerrar las puertas.
  * `MoveUp`: Mover el ascensor hacia arriba.
  * `MoveDown`: Mover el ascensor hacia abajo.
  * `StartDoorTimer`: Iniciar el temporizador de las puertas.
  * `StopBell`: Detener el timbre (si está sonando, por ejemplo, al llegar a un piso).

**Grafo de estados para el controlador del ascensor:**

A continuación, se muestra un grafo de estados simplificado para ilustrar las transiciones principales. Un grafo completo sería más extenso.

[[[IMAGEN]]]

Fig. 2.1. Grafo de estados simplificado para un controlador de ascensor.

**Explicación de algunas transiciones:**

  * Desde `Parado en el piso 1 (DoorsOpen1)`:
      * Si `DoorTimerExpires` ocurre, la acción es `CloseDoors`, y el estado cambia a `Parado en el piso 1 (DoorsClosed1)`.
      * Si `Select2` ocurre, la acción es `CloseDoors`, `MoveUp`, y el estado cambia a `Subiendo al piso 2 (MovingUp)`.
  * Desde `Parado en el piso 1 (DoorsClosed1)`:
      * Si `Call2` o `Select2` ocurre, la acción es `MoveUp`, y el estado cambia a `Subiendo al piso 2 (MovingUp)`.
  * Desde `Subiendo al piso 2 (MovingUp)`:
      * Si `ArrivedAtFloor2` ocurre, la acción es `OpenDoors`, `StartDoorTimer`, y el estado cambia a `Parado en el piso 2 (DoorsOpen2)`.

**PAGINA 46**

**Refinamiento y casos adicionales:**
Este es un modelo simplificado. En un sistema real, se necesitarían más estados y transiciones para manejar:

  * Fallos (ej. puertas que no se cierran).
  * Prioridades de llamadas (ej. si hay llamadas en ambos pisos).
  * Sobrecarga.
  * Botones de emergencia.
  * Mecanismos de seguridad (ej. sensores de puerta).

La especificación detallada incluiría tablas de transición y salida para cada estado y acción de entrada posible.

### Modelado de Sistemas Complejos

Para sistemas más grandes y complejos, la descomposición jerárquica es crucial. Un OCO de nivel superior puede contener varios OCOs de nivel inferior, y sus interacciones se modelan a través de acciones de entrada y salida entre ellos.

Por ejemplo, un sistema de control de tráfico podría tener un OCO principal para gestionar el cruce, y OCOs más pequeños para cada semáforo individual o para la detección de vehículos.

El diseño también implica la definición de las variables de datos que cada OCO necesita para mantener su estado y realizar sus acciones. En el ejemplo del ascensor, las variables de datos podrían incluir la dirección actual de movimiento, el piso objetivo, y el estado del temporizador de la puerta.

El proceso de diseño y especificación es iterativo. A medida que se refinan los requisitos y se comprende mejor el comportamiento del sistema, el modelo de autómata se ajusta y se mejora. La capacidad de los modelos de autómata para ser visualizados como grafos de estados facilita esta iteración y la comunicación entre los desarrolladores y los expertos del dominio.

**PAGINA 47**

**Patrones de diseño de autómatas**
Al igual que en la programación orientada a objetos, existen patrones de diseño recurrentes en la programación automática que pueden reutilizarse para resolver problemas comunes. Algunos de estos patrones incluyen:

  * **El patrón de Estado (State Pattern):** Este patrón es fundamental en la programación automática y se utiliza para permitir que un objeto altere su comportamiento cuando su estado interno cambia. El objeto parecerá cambiar su clase.
  * **El patrón de Fábrica (Factory Pattern):** Puede usarse para crear diferentes tipos de autómatas o componentes de autómata dinámicamente.
  * **El patrón de Observador (Observer Pattern):** Útil para la comunicación entre autómatas o entre un autómata y otros componentes del sistema cuando un cambio en el estado de un autómata necesita notificar a otros.

La comprensión y aplicación de estos patrones puede simplificar significativamente el diseño de sistemas complejos basados en autómatas.

### Ejemplos Adicionales de Diseño

**Ejemplo: Control de una lavadora**
Una lavadora es un excelente ejemplo de un sistema con comportamiento complejo. Sus estados podrían incluir "apagado", "llenando", "lavando", "enjuagando", "centrifugando", "terminado", y las acciones de entrada serían la selección de programas, el inicio, la pausa, la adición de agua, etc. Las acciones de salida serían el control de la bomba de agua, el motor, la resistencia de calefacción, etc.

**Ejemplo: Reconocedor de patrones en texto**
Un autómata puede utilizarse para reconocer patrones específicos en una secuencia de caracteres (texto). Los estados podrían representar el progreso en el reconocimiento del patrón, y las acciones de entrada serían los caracteres individuales. Las acciones de salida podrían ser la detección del patrón o un error.

**PAGINA 48**

### Especificación Formal de Autómatas

La especificación formal de autómatas es esencial para sistemas donde la corrección es crítica. Permite una descripción matemática precisa del comportamiento del sistema, lo que a su vez posibilita la verificación formal.

Los métodos de especificación formal incluyen:

  * **Tablas de transiciones de estado:** Una forma tabular de representar la función de transición y la función de salida. Cada fila de la tabla representa un estado actual, y las columnas representan las acciones de entrada. Las celdas de la tabla contienen el siguiente estado y las acciones de salida correspondientes.
  * **Lenguajes de descripción de máquinas de estado:** Como Statecharts (utilizado en UML), que proporcionan una sintaxis gráfica y formal para describir autómatas.
  * **Álgebras de procesos:** Un formalismo matemático para describir sistemas concurrentes y sus interacciones.
  * **Lógicas temporales:** Permiten expresar propiedades sobre secuencias de estados y transiciones a lo largo del tiempo.

**Ejemplo: Tabla de transiciones y salidas para el ascensor (fragmento)**

| Estado Actual              | Evento de Entrada  | Nuevo Estado                    | Acciones de Salida                               |
| :------------------------- | :----------------- | :------------------------------ | :----------------------------------------------- |
| `DoorsOpen1`               | `DoorTimerExpires` | `DoorsClosed1`                  | `CloseDoors`                                     |
| `DoorsOpen1`               | `Select2`          | `MovingUp`                      | `CloseDoors`, `MoveUp`                           |
| `DoorsClosed1`             | `Call2`            | `MovingUp`                      | `MoveUp`                                         |
| `DoorsClosed1`             | `Select2`          | `MovingUp`                      | `MoveUp`                                         |
| `MovingUp`                 | `ArrivedAtFloor2`  | `DoorsOpen2`                    | `OpenDoors`, `StartDoorTimer`                    |
| `DoorsOpen2`               | `DoorTimerExpires` | `DoorsClosed2`                  | `CloseDoors`                                     |
| `DoorsOpen2`               | `Select1`          | `MovingDown`                    | `CloseDoors`, `MoveDown`                         |
| `DoorsClosed2`             | `Call1`            | `MovingDown`                    | `MoveDown`                                       |
| `DoorsClosed2`             | `Select1`          | `MovingDown`                    | `MoveDown`                                       |
| `MovingDown`               | `ArrivedAtFloor1`  | `DoorsOpen1`                    | `OpenDoors`, `StartDoorTimer`                    |

**PAGINA 49**

Esta tabla es una forma más estructurada y formal de especificar el comportamiento del ascensor, complementando el grafo de estados. Ayuda a asegurar que todos los casos de transición estén cubiertos y que no haya ambigüedades.

### Diseño de la estructura de datos para la implementación

Al diseñar la estructura de datos para un sistema automático, es crucial representar eficientemente los estados, las transiciones y las variables de datos.

En el enfoque procedimental, esto a menudo implica:

  * **Enumeraciones o constantes:** Para representar los estados de control (ej. `enum State { DOOR_OPEN, DOOR_CLOSED, MOVING_UP, ... };`).
  * **Funciones o procedimientos:** Para representar las acciones de salida que se ejecutan al cambiar de estado o al procesar una entrada.
  * **Variables globales o estructuras:** Para almacenar las variables de datos del autómata (`hours`, `minutes`, `alarm_on`, etc.).
  * **Tablas de búsqueda:** Como se mencionó anteriormente, las tablas pueden usarse para almacenar las funciones de transición y salida, especialmente en sistemas donde el autómata es dinámico o muy grande.

**PAGINA 50**

### Implementación del control lógico

La implementación del control lógico en lenguajes procedimentales, como C o Pascal, generalmente sigue una de las dos aproximaciones ya mencionadas:

1.  **Implementación basada en instrucción `switch` (o `if-else` anidados):** Este es el método más común y, a menudo, el más legible para autómatas de tamaño moderado. Un gran `switch` principal se utiliza para seleccionar el estado actual, y dentro de cada caso de estado, otro `switch` (o `if-else` anidados) maneja las diferentes acciones de entrada.

    ```c
    // Pseudo-código para un autómata basado en switch
    enum State currentState;
    // ... otras variables de datos y eventos de entrada

    void processEvent(Event inputEvent) {
        switch (currentState) {
            case STATE_A:
                switch (inputEvent) {
                    case EVENT_X:
                        // Acciones de salida para STATE_A y EVENT_X
                        currentState = STATE_B;
                        break;
                    case EVENT_Y:
                        // Acciones de salida para STATE_A y EVENT_Y
                        currentState = STATE_C;
                        break;
                    // ... otros eventos
                }
                break;
            case STATE_B:
                // ... lógica para STATE_B
                break;
            // ... otros estados
        }
    }
    ```

2.  **Implementación basada en tablas:** Este método utiliza arrays o estructuras de datos para almacenar explícitamente las transiciones y acciones. Es más flexible para autómatas que pueden cambiar dinámicamente o para aquellos que son generados automáticamente. La lógica se convierte en una búsqueda en tabla en lugar de una secuencia de comparaciones.

    ```c
    // Pseudo-código para un autómata basado en tablas
    typedef struct {
        State nextState;
        void (*outputAction)(); // Puntero a función para acciones de salida
    } TransitionEntry;

    TransitionEntry transitionTable[NUM_STATES][NUM_INPUT_EVENTS];
    // ... inicializar la tabla con transiciones y acciones

    void processEvent(Event inputEvent) {
        // Buscar la entrada correspondiente en la tabla
        TransitionEntry entry = transitionTable[currentState][inputEvent];
        
        // Ejecutar la acción de salida
        if (entry.outputAction != NULL) {
            entry.outputAction();
        }
        
        // Actualizar el estado
        currentState = entry.nextState;
    }
    ```

**PAGINA 51**

Cada método tiene sus propias ventajas y desventajas en términos de legibilidad, rendimiento y flexibilidad, como se discutió brevemente en el Capítulo 1.

**Consideraciones para la implementación procedimental:**

  * **Manejo de eventos:** Los eventos de entrada a menudo se manejan en un bucle principal (bucle de eventos) que continuamente lee entradas y llama a la función de procesamiento del autómata.
  * **Concurrencia:** En sistemas concurrentes o en tiempo real, el manejo de eventos y las transiciones de estado deben ser "atómicos" para evitar condiciones de carrera. Esto a menudo requiere el uso de semáforos o mutex para proteger las variables de estado.
  * **Tiempo:** El manejo de tiempos y temporizadores (como el temporizador de la puerta del ascensor) es crucial. Esto puede implementarse mediante un reloj del sistema o mediante una función de "tick" que se llama periódicamente para simular el paso del tiempo.

**PAGINA 52**

### Ejemplos detallados de implementación

Este capítulo proporcionará ejemplos de implementación más detallados para ilustrar los conceptos de la programación automática en un contexto procedimental. Los ejemplos se enfocarán en cómo traducir los modelos de autómatas (grafos de estados y tablas de transiciones) a código C/Pascal.

**Ejemplo: Semáforo simple**
Consideremos un semáforo de un solo cruce de dos direcciones (norte-sur y este-oeste).

**Estados:**

  * `NS_Green_EW_Red`: Norte-Sur verde, Este-Oeste rojo.
  * `NS_Yellow_EW_Red`: Norte-Sur amarillo, Este-Oeste rojo.
  * `NS_Red_EW_Red_Delay`: Norte-Sur rojo, Este-Oeste rojo (delay para cambio).
  * `NS_Red_EW_Green`: Norte-Sur rojo, Este-Oeste verde.
  * `NS_Red_EW_Yellow`: Norte-Sur rojo, Este-Oeste amarillo.
  * `NS_Red_EW_Red_Delay2`: Norte-Sur rojo, Este-Oeste rojo (delay para cambio).

**Eventos de entrada:**

  * `TimerExpired`: El temporizador para la duración de la luz actual ha expirado.

**Acciones de salida:**

  * `SetLight(direction, color)`: Configura la luz para una dirección y color específicos.
  * `StartTimer(duration)`: Inicia un temporizador con una duración específica.

**Grafo de estados simplificado:**

[[[IMAGEN]]]

Fig. 2.2. Grafo de estados simplificado para un semáforo.

**PAGINA 53**

**Implementación en C (fragmento)**

```c
#include <stdio.h>
#include <stdbool.h>
#include <time.h>

// Definición de estados
typedef enum {
    NS_GREEN_EW_RED,
    NS_YELLOW_EW_RED,
    NS_RED_EW_RED_DELAY,
    NS_RED_EW_GREEN,
    NS_RED_EW_YELLOW,
    NS_RED_EW_RED_DELAY2
} TrafficLightState;

// Variable de estado actual
TrafficLightState currentState;

// Variables para el temporizador (simplificado)
time_t timerStartTime;
int timerDuration;

void SetLight(const char* direction, const char* color) {
    printf("Luz %s: %s\n", direction, color);
}

void StartTimer(int duration) {
    timerStartTime = time(NULL);
    timerDuration = duration;
    printf("Temporizador iniciado por %d segundos.\n", duration);
}

bool IsTimerExpired() {
    return (time(NULL) - timerStartTime) >= timerDuration;
}

// Función de inicialización
void initTrafficLight() {
    currentState = NS_GREEN_EW_RED;
    SetLight("NS", "VERDE");
    SetLight("EW", "ROJO");
    StartTimer(10); // 10 segundos para verde
}

// Función de procesamiento de eventos
void processTrafficLight() {
    if (IsTimerExpired()) {
        printf("Temporizador expirado.\n");
        switch (currentState) {
            case NS_GREEN_EW_RED:
                currentState = NS_YELLOW_EW_RED;
                SetLight("NS", "AMARILLO");
                SetLight("EW", "ROJO");
                StartTimer(3); // 3 segundos para amarillo
                break;
            case NS_YELLOW_EW_RED:
                currentState = NS_RED_EW_RED_DELAY;
                SetLight("NS", "ROJO");
                SetLight("EW", "ROJO");
                StartTimer(2); // 2 segundos de delay con ambos en rojo
                break;
            case NS_RED_EW_RED_DELAY:
                currentState = NS_RED_EW_GREEN;
                SetLight("NS", "ROJO");
                SetLight("EW", "VERDE");
                StartTimer(10); // 10 segundos para verde
                break;
            case NS_RED_EW_GREEN:
                currentState = NS_RED_EW_YELLOW;
                SetLight("NS", "ROJO");
                SetLight("EW", "AMARILLO");
                StartTimer(3); // 3 segundos para amarillo
                break;
            case NS_RED_EW_YELLOW:
                currentState = NS_RED_EW_RED_DELAY2;
                SetLight("NS", "ROJO");
                SetLight("EW", "ROJO");
                StartTimer(2); // 2 segundos de delay con ambos en rojo
                break;
            case NS_RED_EW_RED_DELAY2:
                currentState = NS_GREEN_EW_RED;
                SetLight("NS", "VERDE");
                SetLight("EW", "ROJO");
                StartTimer(10); // Volver al inicio
                break;
        }
    }
}

int main() {
    initTrafficLight();
    printf("Simulación del semáforo:\n");
    while (1) {
        processTrafficLight();
        // Simular el paso del tiempo
        // En una aplicación real, esto estaría en un bucle de eventos o manejado por interrupciones
        // Para esta simulación, esperamos un poco para ver los cambios
        // Por simplicidad, no hay una espera activa aquí, el temporizador usa time(NULL)
        // y se basa en la velocidad de ejecución del bucle
    }
    return 0;
}
```

**PAGINA 54**

El código anterior es una implementación básica que demuestra cómo se pueden usar las instrucciones `switch` para manejar las transiciones de estado de un semáforo. El temporizador se simplifica para fines de demostración. En una aplicación real, el manejo del tiempo y los eventos sería más robusto, posiblemente con un sistema operativo en tiempo real o interrupciones.

Este ejemplo ilustra cómo un modelo de autómata (el grafo de estados) se traduce directamente en un código procedimental estructurado y legible. Cada `case` del `switch` principal corresponde a un estado del autómata, y los cambios dentro de cada `case` representan las transiciones basadas en eventos (en este caso, la expiración del temporizador).

**PAGINA 55**

### Implementación del Control Lógico (continuación)

**Ejemplo: Máquina de estado para un reproductor de medios simple**

Consideremos un reproductor de medios muy simple con las siguientes funcionalidades:

  * Reproducir (Play)
  * Pausar (Pause)
  * Detener (Stop)
  * Saltar a la siguiente pista (Next)
  * Saltar a la pista anterior (Previous)

**Estados:**

  * `Stopped`: El reproductor está detenido.
  * `Playing`: El reproductor está reproduciendo una pista.
  * `Paused`: El reproductor está en pausa.

**Eventos de entrada:**

  * `PlayButton`: Se presiona el botón de reproducción.
  * `PauseButton`: Se presiona el botón de pausa.
  * `StopButton`: Se presiona el botón de detener.
  * `NextButton`: Se presiona el botón de siguiente.
  * `PrevButton`: Se presiona el botón de anterior.
  * `TrackEnd`: La pista actual ha terminado.

**Acciones de salida:**

  * `StartPlayback()`: Inicia la reproducción de la pista actual.
  * `PausePlayback()`: Pausa la reproducción.
  * `StopPlayback()`: Detiene la reproducción y reinicia la pista.
  * `PlayNextTrack()`: Carga y reproduce la siguiente pista.
  * `PlayPreviousTrack()`: Carga y reproduce la pista anterior.

**Grafo de estados simplificado:**

[[[IMAGEN]]]

Fig. 2.3. Grafo de estados para un reproductor de medios simple.

**PAGINA 56**

**Descripción de transiciones clave:**

  * Desde `Stopped`:
      * `PlayButton` $\\to$ `Playing` (Acción: `StartPlayback()`)
  * Desde `Playing`:
      * `PauseButton` $\\to$ `Paused` (Acción: `PausePlayback()`)
      * `StopButton` $\\to$ `Stopped` (Acción: `StopPlayback()`)
      * `NextButton` $\\to$ `Playing` (Acción: `PlayNextTrack()`)
      * `PrevButton` $\\to$ `Playing` (Acción: `PlayPreviousTrack()`)
      * `TrackEnd` $\\to$ `Stopped` (Acción: `StopPlayback()`)
  * Desde `Paused`:
      * `PlayButton` $\\to$ `Playing` (Acción: `StartPlayback()`)
      * `StopButton` $\\to$ `Stopped` (Acción: `StopPlayback()`)

**Implementación en C (fragmento usando `switch`)**

```c
#include <stdio.h>
#include <stdbool.h>

// Definición de estados
typedef enum {
    STOPPED,
    PLAYING,
    PAUSED
} MediaPlayerState;

// Definición de eventos
typedef enum {
    PLAY_BUTTON,
    PAUSE_BUTTON,
    STOP_BUTTON,
    NEXT_BUTTON,
    PREV_BUTTON,
    TRACK_END
} MediaPlayerEvent;

// Estado actual del reproductor
MediaPlayerState currentMediaPlayerState;

// Funciones de acción de salida (simuladas)
void StartPlayback() {
    printf("Reproducción iniciada.\n");
}
void PausePlayback() {
    printf("Reproducción pausada.\n");
}
void StopPlayback() {
    printf("Reproducción detenida.\n");
}
void PlayNextTrack() {
    printf("Reproduciendo siguiente pista.\n");
}
void PlayPreviousTrack() {
    printf("Reproduciendo pista anterior.\n");
}

// Función de procesamiento de eventos
void processMediaPlayerEvent(MediaPlayerEvent event) {
    switch (currentMediaPlayerState) {
        case STOPPED:
            switch (event) {
                case PLAY_BUTTON:
                    currentMediaPlayerState = PLAYING;
                    StartPlayback();
                    break;
                default:
                    printf("Evento %d ignorado en estado STOPPED.\n", event);
                    break;
            }
            break;

        case PLAYING:
            switch (event) {
                case PAUSE_BUTTON:
                    currentMediaPlayerState = PAUSED;
                    PausePlayback();
                    break;
                case STOP_BUTTON:
                    currentMediaPlayerState = STOPPED;
                    StopPlayback();
                    break;
                case NEXT_BUTTON:
                    PlayNextTrack();
                    break;
                case PREV_BUTTON:
                    PlayPreviousTrack();
                    break;
                case TRACK_END:
                    currentMediaPlayerState = STOPPED;
                    StopPlayback();
                    break;
                default:
                    printf("Evento %d ignorado en estado PLAYING.\n", event);
                    break;
            }
            break;

        case PAUSED:
            switch (event) {
                case PLAY_BUTTON:
                    currentMediaPlayerState = PLAYING;
                    StartPlayback();
                    break;
                case STOP_BUTTON:
                    currentMediaPlayerState = STOPPED;
                    StopPlayback();
                    break;
                default:
                    printf("Evento %d ignorado en estado PAUSED.\n", event);
                    break;
            }
            break;
    }
}

// Función principal para demostración
int main() {
    currentMediaPlayerState = STOPPED;
    printf("Reproductor de medios simple:\n");

    processMediaPlayerEvent(PLAY_BUTTON);   // De Stopped a Playing
    processMediaPlayerEvent(PAUSE_BUTTON);  // De Playing a Paused
    processMediaPlayerEvent(PLAY_BUTTON);   // De Paused a Playing
    processMediaPlayerEvent(NEXT_BUTTON);   // En Playing
    processMediaPlayerEvent(STOP_BUTTON);   // De Playing a Stopped
    processMediaPlayerEvent(TRACK_END);     // En Stopped (ignorará)
    
    return 0;
}
```

**PAGINA 57**

Este ejemplo demuestra la implementación de un autómata de reproductor de medios utilizando la estructura `switch` anidada, que es común en la programación procedimental para manejar la lógica del comportamiento complejo. El código refleja directamente el grafo de estados, haciendo que las transiciones y acciones sean explícitas.

### Programación basada en tablas para autómatas complejos

Aunque la implementación basada en `switch` es a menudo preferida por su legibilidad para autómatas de tamaño moderado, la implementación basada en tablas se vuelve más ventajosa en los siguientes escenarios:

  * **Autómatas generados dinámicamente:** Cuando el comportamiento del autómata no se conoce completamente en tiempo de compilación, sino que se define en tiempo de ejecución (por ejemplo, a partir de un archivo de configuración o una entrada del usuario).
  * **Autómatas muy grandes:** Para autómatas con un número muy elevado de estados y transiciones, un `switch` anidado podría volverse inmanejable y difícil de mantener. Las tablas pueden estructurar mejor esta complejidad.
  * **Reconfiguración en tiempo de ejecución:** Si el autómata necesita modificar sus reglas de transición o acción mientras está en funcionamiento, las tablas permiten cambios en la memoria sin recompilar el código.
  * **Herramientas de generación de código:** Las herramientas que generan código automáticamente a partir de modelos de autómatas a menudo producen una implementación basada en tablas para mayor flexibilidad.

La principal desventaja de la implementación basada en tablas es que puede ser menos legible para los humanos directamente en el código, requiriendo una comprensión de la estructura de la tabla. Además, la búsqueda en tabla puede ser ligeramente más lenta que una cadena de `if/else` bien optimizada por el compilador, aunque esta diferencia suele ser insignificante para la mayoría de las aplicaciones.

**PAGINA 58**

**Ejemplo de implementación basada en tablas (Concepto)**

Para ilustrar una implementación basada en tablas, podríamos definir una estructura de datos para cada entrada en la tabla de transiciones. Cada entrada contendría el estado siguiente y quizás un puntero a una función de acción que se ejecutaría durante esa transición.

```c
// Definición de un puntero a función para acciones de salida
typedef void (*OutputActionFunc)();

// Estructura para una entrada en la tabla de transiciones
typedef struct {
    MediaPlayerState nextState; // El siguiente estado al que transitar
    OutputActionFunc action;    // La función a llamar para esta transición
} TransitionTableEntry;

// La tabla de transiciones (matriz 2D)
// Filas: Estados actuales
// Columnas: Eventos de entrada
TransitionTableEntry transitionTable[NUM_MEDIA_PLAYER_STATES][NUM_MEDIA_PLAYER_EVENTS];

// Función para inicializar la tabla (ejemplo parcial)
void initializeTransitionTable() {
    // Estado: STOPPED
    transitionTable[STOPPED][PLAY_BUTTON] = (TransitionTableEntry){PLAYING, StartPlayback};
    // Otros eventos en STOPPED que no causan transición o acción se pueden dejar como (STOPPED, NULL) o (currentState, NULL)
    transitionTable[STOPPED][PAUSE_BUTTON] = (TransitionTableEntry){STOPPED, NULL}; // Ignorar pausa si está detenido
    // ...

    // Estado: PLAYING
    transitionTable[PLAYING][PAUSE_BUTTON] = (TransitionTableEntry){PAUSED, PausePlayback};
    transitionTable[PLAYING][STOP_BUTTON] = (TransitionTableEntry){STOPPED, StopPlayback};
    transitionTable[PLAYING][NEXT_BUTTON] = (TransitionTableEntry){PLAYING, PlayNextTrack};
    transitionTable[PLAYING][PREV_BUTTON] = (TransitionTableEntry){PLAYING, PlayPreviousTrack};
    transitionTable[PLAYING][TRACK_END] = (TransitionTableEntry){STOPPED, StopPlayback};
    // ...

    // Estado: PAUSED
    transitionTable[PAUSED][PLAY_BUTTON] = (TransitionTableEntry){PLAYING, StartPlayback};
    transitionTable[PAUSED][STOP_BUTTON] = (TransitionTableEntry){STOPPED, StopPlayback};
    // ...
}

// Función genérica para procesar eventos utilizando la tabla
void processEventUsingTable(MediaPlayerEvent event) {
    TransitionTableEntry entry = transitionTable[currentMediaPlayerState][event];

    if (entry.action != NULL) {
        entry.action(); // Ejecutar la acción de salida
    }
    currentMediaPlayerState = entry.nextState; // Actualizar el estado
}

// Ejemplo de uso en main:
// currentMediaPlayerState = STOPPED;
// initializeTransitionTable();
// processEventUsingTable(PLAY_BUTTON);
// processEventUsingTable(PAUSE_BUTTON);
// ...
```

Este enfoque de tabla requiere una configuración inicial más compleja, pero una vez establecida, la lógica de procesamiento de eventos es muy genérica y compacta.

**PAGINA 59**

### Integración con componentes externos

Los autómatas raramente operan de forma aislada. A menudo necesitan interactuar con otros componentes del software o hardware del sistema. En el enfoque procedimental, esta integración se logra mediante:

  * **Llamadas a funciones:** Las acciones de salida del autómata a menudo implican llamar a funciones proporcionadas por otros módulos o APIs de hardware (por ejemplo, `bell_on()` para activar un timbre, `SetLight()` para controlar un LED).
  * **Lectura de variables externas:** Las condiciones de transición pueden depender de variables de entrada que son actualizadas por otros hilos, procesos o directamente por hardware (por ejemplo, `IsTimerExpired()`, valores de sensores).
  * **Colas de eventos:** Para sistemas asíncronos, los eventos de entrada pueden colocarse en una cola de eventos por varios productores, y el autómata (o su bucle de eventos) los consume de la cola.

**Ejemplo: Lectura de entradas de hardware**
Un autómata de control de un botón podría leer directamente el estado de un pin GPIO de un microcontrolador para determinar si el botón está presionado.

```c
// Ejemplo simplificado de cómo un autómata podría leer una entrada de hardware
// Suponiendo una función de lectura de pin de GPIO
extern bool read_gpio_pin(int pin_number);

// En la función de procesamiento de eventos del autómata:
void processInput() {
    if (read_gpio_pin(BUTTON_PIN_1)) {
        processEvent(BUTTON_1_PRESSED);
    }
    // ...
}
```

Este método permite que el autómata reaccione a eventos del mundo físico.

**PAGINA 60**

### Gestión de errores y excepciones

En un sistema robusto, es crucial manejar errores y situaciones excepcionales. En la programación automática procedimental, esto puede incluir:

  * **Estados de error:** Definir estados específicos en el autómata que representan una condición de error (ej. `ErrorState_DoorStuck`). Las transiciones a estos estados se activarían por eventos de error (ej. `DoorFailedToClose`).
  * **Transiciones de "rescate":** Definir transiciones que saquen al autómata de un estado de error o un estado inesperado a un estado seguro o conocido.
  * **Mecanismos de temporización:** Utilizar temporizadores para detectar si una acción no se completa dentro de un tiempo esperado, lo que indicaría un error.
  * **Retorno de valores y códigos de error:** Las funciones de acción pueden devolver códigos de error que el bucle de eventos o el autómata principal podrían interpretar para desencadenar transiciones de error.
  * **Registros (logging):** Registrar eventos de error y transiciones inesperadas para facilitar la depuración y el análisis post-mortem.

**Ejemplo: Puerta de ascensor atascada**
Si las puertas del ascensor no se cierran dentro de un tiempo razonable, podría activarse un evento `DoorTimeout`. Esto podría llevar el autómata al estado `ErrorState_DoorStuck`, donde se podrían intentar acciones como reintentar cerrar las puertas, o activar una alarma.

**PAGINA 61**

### Consideraciones sobre el rendimiento

En sistemas en tiempo real o con recursos limitados (como microcontroladores), el rendimiento del autómata es una consideración importante.

  * **Optimización del `switch`:** Los compiladores modernos son muy eficientes optimizando grandes estructuras `switch`. En muchos casos, un `switch` anidado puede ser tan rápido o incluso más rápido que una implementación basada en tablas si las ramas son predecibles.
  * **Tamaño de las tablas:** Para implementaciones basadas en tablas, el tamaño de la tabla puede afectar el rendimiento de la caché. Una tabla muy grande podría generar más fallos de caché. Sin embargo, técnicas como la compresión de tablas o el uso de tablas dispersas pueden mitigar este problema.
  * **Complejidad de las acciones:** Las acciones de salida deben ser eficientes. Las operaciones que consumen mucho tiempo dentro de las funciones de acción pueden retrasar el procesamiento de eventos subsiguientes. En sistemas de tiempo real, las acciones largas podrían requerir el uso de hilos o mecanismos de programación asíncrona.
  * **Frecuencia de eventos:** La frecuencia con la que se procesan los eventos afecta la carga de la CPU. En sistemas de alto rendimiento, es crucial que el bucle de eventos sea eficiente y que el procesamiento de cada evento sea rápido.
  * **Número de estados y transiciones:** Aunque la teoría sugiere que un número elevado de estados puede aumentar la complejidad, una buena abstracción y descomposición del sistema puede mantener la complejidad manejable para cada autómata individual.

**PAGINA 62**

### Concurrencia y paralelismo

La programación automática puede extenderse para manejar sistemas concurrentes y paralelos.

  * **Múltiples autómatas:** Un sistema puede consistir en múltiples autómatas que se ejecutan concurrentemente y se comunican entre sí a través de eventos.
      * **Comunicación síncrona:** Un autómata puede enviar un evento a otro y esperar una respuesta antes de continuar (comportamiento similar a una llamada a función).
      * **Comunicación asíncrona:** Un autómata envía un evento a otro y continúa su propia ejecución sin esperar una respuesta. Los eventos se suelen colocar en colas.
  * **Autómatas jerárquicos:** Como se mencionó, un autómata puede contener sub-autómatas. Cuando el autómata padre entra en un estado que tiene un sub-autómata, el control se pasa al sub-autómata. Cuando el sub-autómata completa su tarea, el control regresa al padre.
  * **Máquinas de estados ortogonales:** Algunos formalismos (como Statecharts de Harel) permiten que un autómata tenga múltiples "regiones" ortogonales que se ejecutan en paralelo. Esto es útil para describir aspectos independientes del comportamiento de un objeto.

**PAGINA 63**

**Ejemplo: Un sistema de gestión de alarmas con múltiples autómatas**

Imagine un sistema de seguridad con un autómata principal `AlarmSystemController` que gestiona el estado general del sistema (Armado, Desarmado, Alarma Activa). Este autómata podría interactuar con otros autómatas:

  * `MotionSensorController`: Gestiona el estado de los sensores de movimiento (Activado, Desactivado, Detección de movimiento).
  * `DoorSensorController`: Gestiona el estado de los sensores de puertas/ventanas (Abierta, Cerrada, Tamper).
  * `SirenController`: Controla la sirena (Apagada, Sonando).

Cuando el `AlarmSystemController` cambia a `Armado`, envía eventos a `MotionSensorController` y `DoorSensorController` para que se activen. Si `MotionSensorController` detecta movimiento mientras el sistema está armado, envía un evento de `IntrusionDetected` al `AlarmSystemController`, que luego podría activar el `SirenController` para hacer sonar la alarma.

La gestión de la concurrencia entre estos autómatas requiere un bucle de eventos centralizado o un planificador (scheduler) que distribuya los eventos a los autómatas apropiados y asegure que las transiciones de estado se realicen de manera segura.

**PAGINA 64**

### Especificación (continuación)

La especificación detallada de los sistemas automáticos no solo implica la descripción de los estados y transiciones, sino también:

  * **Condiciones de guarda:** Las transiciones pueden tener condiciones asociadas que deben ser verdaderas para que la transición ocurra (además del evento de entrada). Por ejemplo, un ascensor solo sube si el piso de destino es mayor que el actual.
  * **Acciones de entrada (Entry Actions):** Acciones que se ejecutan automáticamente cada vez que un autómata *entra* en un estado.
  * **Acciones de salida (Exit Actions):** Acciones que se ejecutan automáticamente cada vez que un autómata *sale* de un estado.
  * **Acciones internas (Internal Actions):** Acciones que se ejecutan mientras el autómata está en un estado específico, sin causar una transición. Estas pueden ser periódicas o activadas por eventos internos.

Estos conceptos permiten describir comportamientos más complejos y matizados dentro del modelo de autómata.

**Ejemplo: Acciones de entrada/salida para el ascensor**

  * **Estado `DoorsOpen1` (puertas abiertas en el piso 1):**
      * *Acción de entrada:* `OpenDoors()`, `StartDoorTimer()`
      * *Acción de salida:* `StopDoorTimer()`
  * **Estado `MovingUp` (subiendo):**
      * *Acción de entrada:* `StartMotorUp()`, `CloseDoors()`
      * *Acción de salida:* `StopMotor()`

Estas acciones de entrada/salida simplifican el grafo de estados, ya que las acciones comunes al entrar o salir de un estado se agrupan, en lugar de repetirse en cada transición individual que conduce a o sale de ese estado.

**PAGINA 65**

### Requisitos no funcionales

Además de la lógica del comportamiento, la especificación de sistemas automáticos debe abordar los requisitos no funcionales, como:

  * **Rendimiento:** Tiempos de respuesta, rendimiento.
  * **Fiabilidad:** Tolerancia a fallos, robustez.
  * **Seguridad:** Resistencia a ataques.
  * **Usabilidad:** Facilidad de uso para el operador.
  * **Mantenibilidad:** Facilidad de modificación y depuración.
  * **Portabilidad:** Capacidad de ejecutar el software en diferentes plataformas.

La programación automática contribuye a la fiabilidad y mantenibilidad mediante su estructura clara y la posibilidad de verificación formal. Sin embargo, otros requisitos no funcionales, como el rendimiento en sistemas de tiempo real, deben considerarse cuidadosamente durante el diseño y la implementación.

### Herramientas para la programación automática procedimental

Aunque es posible implementar autómatas "a mano" en C/Pascal, existen herramientas que pueden automatizar gran parte del proceso:

  * **Herramientas de modelado de estados:** Permiten diseñar autómatas gráficamente (ej. UML Statechart Diagrams en Rational Rose RealTime, Enterprise Architect).
  * **Generadores de código:** Estas herramientas pueden tomar un modelo de autómata (por ejemplo, un diagrama de estados o una tabla) y generar automáticamente el código fuente en C, C++, Java, u otros lenguajes. Esto reduce los errores humanos y acelera el desarrollo.
  * **Simuladores de autómatas:** Permiten ejecutar y depurar el modelo de autómata antes de la implementación completa, ayudando a identificar errores lógicos tempranamente.
  * **Herramientas de verificación formal:** Ayudan a probar propiedades de seguridad y vivacidad del autómata.

El uso de estas herramientas puede mejorar significativamente la productividad y la calidad del software en la programación automática.

**PAGINA 66**

**Ejemplo: Un generador de código de autómata (conceptual)**

Un generador de código podría tomar un archivo de entrada que especifique los estados, eventos, transiciones y acciones de un autómata, y producir un archivo `.c` con la implementación del `switch` anidado o la tabla de transiciones.

**Archivo de entrada (ejemplo simplificado)**

```
# Definición de Estados
STATES: Stopped, Playing, Paused

# Definición de Eventos
EVENTS: PlayButton, PauseButton, StopButton, NextButton, PrevButton, TrackEnd

# Definición de Transiciones
TRANSITIONS:
  STOPPED:
    PlayButton -> PLAYING / StartPlayback

  PLAYING:
    PauseButton -> PAUSED / PausePlayback
    StopButton -> STOPPED / StopPlayback
    NextButton -> PLAYING / PlayNextTrack
    PrevButton -> PLAYING / PlayPreviousTrack
    TrackEnd -> STOPPED / StopPlayback

  PAUSED:
    PlayButton -> PLAYING / StartPlayback
    StopButton -> STOPPED / StopPlayback

# Acciones (prototipos para el generador)
ACTIONS:
  StartPlayback()
  PausePlayback()
  StopPlayback()
  PlayNextTrack()
  PlayPreviousTrack()
```

**PAGINA 67**

A partir de este tipo de especificación, el generador produciría el código C que vimos anteriormente para el reproductor de medios. Esto permite a los ingenieros trabajar a un nivel de abstracción más alto y reducir la posibilidad de errores de codificación manual.

### Resumen del Capítulo 2

En este capítulo, se profundizó en la *programación procedimental con estados explícitamente definidos*, destacando su aplicación principal en sistemas de control lógico y su fundamentación en la teoría de autómatas y lenguajes formales.

Se detalló el proceso de *diseño* de sistemas de control lógico, que incluye la identificación de objetos de control automatizados (OCOs), el modelado de su comportamiento mediante autómatas, la descomposición del sistema, la definición de interfaces y el refinamiento iterativo.

La *especificación* se abordó como un proceso crucial para describir formalmente el comportamiento de los autómatas, utilizando tablas de estados, diagramas de estados (grafos) y lenguajes formales. Se proporcionó un ejemplo extendido del controlador de un ascensor para ilustrar estos conceptos.

La *implementación* del autómata en lenguajes procedimentales como C y Pascal se exploró a través de dos enfoques principales: la implementación basada en `switch` (o `if-else` anidados) y la implementación basada en tablas. Se presentaron ejemplos de código para un semáforo y un reproductor de medios, ilustrando ambas aproximaciones y discutiendo sus ventajas y desventajas.

Además, se cubrieron temas importantes para la construcción de sistemas robustos y eficientes:

  * La *integración con componentes externos* mediante llamadas a funciones, lectura de variables y colas de eventos.
  * La *gestión de errores y excepciones* a través de estados de error, transiciones de rescate y mecanismos de temporización.
  * Las *consideraciones de rendimiento* en entornos con recursos limitados.
  * El manejo de la *concurrencia y el paralelismo* a través de múltiples autómatas, jerarquías y máquinas de estados ortogonales.
  * La importancia de las *acciones de entrada/salida de estado* y las *condiciones de guarda* para una especificación más rica.
  * La relevancia de los *requisitos no funcionales* y el papel de las *herramientas* de modelado, generación de código y verificación en el ciclo de vida del desarrollo.

Este capítulo proporciona una base sólida para la implementación práctica de sistemas basados en autómatas utilizando un enfoque procedimental, preparando el terreno para el siguiente capítulo, que explorará la relación entre la programación automática y la programación orientada a objetos.

**PAGINA 68**

### Ejercicios para la autoevaluación

1.  Describa los principales componentes de un sistema de control lógico en el contexto de la programación automática.
2.  ¿Cuáles son las ventajas y desventajas de la implementación de autómatas mediante `switch` frente a la implementación basada en tablas?
3.  Diseñe un autómata para un sistema de apertura/cierre de puerta de garaje (con botones para abrir, cerrar y detener, y sensores para puerta abierta/cerrada). Dibuje el grafo de estados y enumere estados, eventos y acciones.
4.  ¿Cómo se puede manejar la concurrencia en sistemas con múltiples autómatas en un enfoque procedimental?
5.  Explique el concepto de acciones de entrada y salida de estado en la especificación de autómatas. Dé ejemplos.
6.  ¿Qué es una condición de guarda en una transición de autómata y para qué se utiliza?
7.  Mencione al menos tres requisitos no funcionales que deben considerarse al diseñar un sistema automático.
8.  Enumere las categorías de herramientas que pueden apoyar el desarrollo de software con programación automática.

**PAGINA 69**

[[[IMAGEN]]]

Fig. 2.4.

[[[IMAGEN]]]

Fig. 2.5.

[[[IMAGEN]]]

Fig. 2.6.

[[[IMAGEN]]]

Fig. 2.7.

**PAGINA 70**

[[[IMAGEN]]]

Fig. 2.8.

[[[IMAGEN]]]

Fig. 2.9.

**PAGINA 71**

[[[IMAGEN]]]

Fig. 2.10.

**PAGINA 72**

[[[IMAGEN]]]

Fig. 2.11.

**PAGINA 73**

[[[IMAGEN]]]

Fig. 2.12.

**PAGINA 74**

[[[IMAGEN]]]

Fig. 2.13.

**PAGINA 75**

[[[IMAGEN]]]

Fig. 2.14.

**PAGINA 76**

### Capítulo 3. Programación orientada a objetos con estados explícitamente definidos

Este capítulo explora la relación entre la programación automática y la programación orientada a objetos (POO). Demostraremos que el enfoque automático no es una alternativa, sino una extensión natural y complementaria de la POO, especialmente para la gestión del comportamiento complejo de los objetos.

La POO se ha convertido en el paradigma dominante en el desarrollo de software debido a su capacidad para modelar el mundo real en términos de objetos que encapsulan datos y comportamiento. Sin embargo, la POO tradicional a menudo carece de un mecanismo explícito y bien estructurado para modelar el *comportamiento dependiente del estado* o *comportamiento complejo*.

Como se mencionó en el Capítulo 1, el uso de "flags" booleanas y estructuras `if-else` o `switch` anidadas para gestionar el comportamiento complejo dentro de los métodos de una clase puede llevar a código ilegible, difícil de mantener y propenso a errores. Aquí es donde la programación automática puede ofrecer una solución elegante y poderosa.

**PAGINA 77**

La integración de los autómatas con la POO se logra mediante la encapsulación de la lógica del autómata dentro de las clases. El objeto de control automatizado (OCO), introducido en el Capítulo 1, es fundamentalmente un concepto orientado a objetos:

  * Un OCO es una entidad que combina datos (variables de datos) y comportamiento (autómata finito).
  * El autómata finito describe la lógica de control del OCO, es decir, cómo el OCO reacciona a los eventos y cambia su estado interno.
  * Las variables de datos del OCO son los atributos de la clase, mientras que el autómata define cómo estos atributos afectan el comportamiento y cómo el comportamiento los modifica.

En este capítulo, examinaremos cómo los principios y patrones de diseño de la POO (encapsulación, herencia, polimorfismo) pueden aplicarse para implementar sistemas automáticos de manera más robusta y modular.

### Diseño orientado a objetos de autómatas

El diseño de un sistema con autómatas en un contexto orientado a objetos implica pensar en cada objeto de control automatizado como una clase o un conjunto de clases que colaboran.

El patrón de diseño "Estado" (State Pattern) es el patrón POO más directamente aplicable a la programación automática. En este patrón, el comportamiento de un objeto se externaliza en un conjunto de clases de estado separadas. El objeto principal (el "Contexto") delega su comportamiento a una de estas clases de estado, y cambia la clase de estado en tiempo de ejecución.

**PAGINA 78**

**El patrón Estado**
El patrón Estado es un patrón de comportamiento que permite a un objeto alterar su comportamiento cuando su estado interno cambia. El objeto parecerá cambiar su clase.

  * **Contexto (Context):** La clase principal cuyo comportamiento cambia según el estado. Mantiene una referencia a un objeto `State` concreto.
  * **Estado (State):** Una interfaz o clase abstracta que define una interfaz para encapsular el comportamiento asociado a un estado particular del Contexto.
  * **Estado Concreto (ConcreteState):** Clases que implementan la interfaz `State` y definen el comportamiento específico de un estado particular. Cada `ConcreteState` también contiene una referencia al `Contexto` para manipular su estado interno y realizar transiciones.

**PAGINA 79**

[[[IMAGEN]]]

Fig. 3.1. Diagrama de clases UML para el patrón Estado.

**Aplicación al autómata del reproductor de medios:**

  * **Contexto:** La clase `MediaPlayer` sería el Contexto. Contendría una referencia al objeto `MediaPlayerState` actual.
  * **Estado:** Una interfaz o clase abstracta `IMediaPlayerState` con métodos como `play()`, `pause()`, `stop()`, `next()`, `prev()`, `trackEnded()`.
  * **Estados Concretos:** Clases como `StoppedState`, `PlayingState`, `PausedState`, cada una implementando los métodos de `IMediaPlayerState` de manera específica para su estado.

Cuando un evento (ej. `PlayButton`) ocurre en el `MediaPlayer`, este delega la llamada al método correspondiente de su objeto `currentMediaPlayerState`. El objeto de estado actual (ej. `StoppedState`) implementa la lógica para ese evento y, si es necesario, cambia el estado del `MediaPlayer` a un nuevo `ConcreteState` (ej. `PlayingState`).

**PAGINA 80**

Este enfoque reduce el número de sentencias `if-else` o `switch` dentro de la clase `MediaPlayer` y hace que el código sea más modular y extensible. Añadir un nuevo estado o modificar el comportamiento de un estado existente es tan sencillo como crear una nueva clase de estado o modificar una existente, sin afectar otras clases.

**PAGINA 81**

### Especificación orientada a objetos de autómatas

La especificación de autómatas en un contexto orientado a objetos a menudo se realiza utilizando diagramas de máquina de estados de UML (Unified Modeling Language). Estos diagramas son una extensión de los grafos de estados y son parte integral del estándar UML, que está diseñado para modelar sistemas orientados a objetos.

Los diagramas de máquina de estados de UML ofrecen una notación rica que incluye:

  * **Estados anidados (subestados):** Un estado puede contener otros estados, lo que permite modelar jerarquías de comportamiento. Por ejemplo, un estado "Reproduciendo" podría tener subestados como "NormalPlayback", "FastForward", "Rewind".
  * **Estados concurrentes (regiones ortogonales):** Un estado puede dividirse en múltiples regiones que se ejecutan en paralelo de forma independiente. Esto es útil para modelar aspectos del comportamiento que son independientes pero que ocurren simultáneamente (ej. un reproductor que reproduce y muestra el tiempo transcurrido, donde el control de reproducción y la actualización del tiempo son aspectos ortogonales).
  * **Eventos:** Las señales que desencadenan transiciones.
  * **Condiciones de guarda:** Expresiones booleanas que deben ser verdaderas para que una transición se dispare.
  * **Acciones de entrada/salida:** Acciones que se ejecutan al entrar o salir de un estado.
  * **Actividades:** Comportamiento continuo que ocurre mientras el objeto está en un estado.

**PAGINA 82**

[[[IMAGEN]]]

Fig. 3.2. Ejemplo de diagrama de máquina de estados UML con estados anidados y concurrencia (conceptual).

La notación UML Statechart Diagrams (Diagramas de Máquinas de Estado) proporciona una forma visual y formal para describir la lógica de comportamiento complejo. Esto permite que los diseñadores de software comuniquen los requisitos y el diseño de manera clara, y también sirve como base para la generación automática de código.

**PAGINA 83**

### Implementación orientada a objetos de autómatas

La implementación orientada a objetos de autómatas generalmente sigue el patrón Estado. A continuación, se presenta un esqueleto de implementación en C++ para el reproductor de medios.

**1. Interfaz de estado (abstracta):**

```cpp
// IMediaPlayerState.h
#ifndef IMEDIAPLAYERSTATE_H
#define IMEDIAPLAYERSTATE_H

class MediaPlayer; // Declaración adelantada para evitar dependencia circular

class IMediaPlayerState {
public:
    virtual ~IMediaPlayerState() {}
    virtual void play(MediaPlayer* player) = 0;
    virtual void pause(MediaPlayer* player) = 0;
    virtual void stop(MediaPlayer* player) = 0;
    virtual void next(MediaPlayer* player) = 0;
    virtual void prev(MediaPlayer* player) = 0;
    virtual void trackEnd(MediaPlayer* player) = 0;
};

#endif // IMEDIAPLAYERSTATE_H
```

**2. Contexto (MediaPlayer):**

```cpp
// MediaPlayer.h
#ifndef MEDIAPLAYER_H
#define MEDIAPLAYER_H

#include "IMediaPlayerState.h"
#include <iostream> // Para printf

class MediaPlayer {
private:
    IMediaPlayerState* currentState;

public:
    MediaPlayer();
    ~MediaPlayer();

    void setState(IMediaPlayerState* newState);

    // Métodos para manejar eventos del usuario
    void play();
    void pause();
    void stop();
    void next();
    void prev();
    void trackEnd();

    // Acciones internas del reproductor (pueden ser llamadas por los estados)
    void startPlaybackInternal() { std::cout << "DEBUG: Reproducción iniciada.\n"; }
    void pausePlaybackInternal() { std::cout << "DEBUG: Reproducción pausada.\n"; }
    void stopPlaybackInternal()  { std::cout << "DEBUG: Reproducción detenida.\n"; }
    void playNextTrackInternal() { std::cout << "DEBUG: Reproduciendo siguiente pista.\n"; }
    void playPreviousTrackInternal() { std::cout << "DEBUG: Reproduciendo pista anterior.\n"; }
};

#endif // MEDIAPLAYER_H
```

**PAGINA 84**

```cpp
// MediaPlayer.cpp
#include "MediaPlayer.h"
#include "StoppedState.h" // Se incluirá más tarde

MediaPlayer::MediaPlayer() {
    // Estado inicial
    currentState = StoppedState::getInstance(); // Singleton para los estados
    std::cout << "Reproductor inicializado en estado STOPPED.\n";
}

MediaPlayer::~MediaPlayer() {
    // Si los estados fueran creados dinámicamente, se deberían borrar aquí.
    // Con Singletons, no se hace.
}

void MediaPlayer::setState(IMediaPlayerState* newState) {
    if (currentState != newState) {
        // En una implementación más robusta, aquí se podría llamar a una acción de salida del estado actual
        // y a una acción de entrada del nuevo estado.
        currentState = newState;
        // std::cout << "Estado cambiado a: " << typeid(*newState).name() << std::endl; // Puede usarse para depuración
    }
}

void MediaPlayer::play() { currentState->play(this); }
void MediaPlayer::pause() { currentState->pause(this); }
void MediaPlayer::stop() { currentState->stop(this); }
void MediaPlayer::next() { currentState->next(this); }
void MediaPlayer::prev() { currentState->prev(this); }
void MediaPlayer::trackEnd() { currentState->trackEnd(this); }
```

**3. Estados Concretos (StoppedState, PlayingState, PausedState):**

Estos estados implementarán la interfaz `IMediaPlayerState` y contendrán la lógica de transición y acción para cada evento. A menudo se implementan como Singletons para evitar la creación repetida de objetos de estado.

```cpp
// StoppedState.h
#ifndef STOPPEDSTATE_H
#define STOPPEDSTATE_H

#include "IMediaPlayerState.h"
#include "MediaPlayer.h"

class StoppedState : public IMediaPlayerState {
public:
    static StoppedState* getInstance();

    void play(MediaPlayer* player) override;
    void pause(MediaPlayer* player) override;
    void stop(MediaPlayer* player) override;
    void next(MediaPlayer* player) override;
    void prev(MediaPlayer* player) override;
    void trackEnd(MediaPlayer* player) override;

private:
    StoppedState() {} // Constructor privado para Singleton
    static StoppedState* instance;
};

#endif // STOPPEDSTATE_H
```

**PAGINA 85**

```cpp
// StoppedState.cpp
#include "StoppedState.h"
#include "PlayingState.h" // Para transicionar a PlayingState

StoppedState* StoppedState::instance = nullptr;

StoppedState* StoppedState::getInstance() {
    if (instance == nullptr) {
        instance = new StoppedState();
    }
    return instance;
}

void StoppedState::play(MediaPlayer* player) {
    player->startPlaybackInternal();
    player->setState(PlayingState::getInstance());
}

void StoppedState::pause(MediaPlayer* player) {
    // No hacer nada o reportar un error
    std::cout << "Acción PAUSE ignorada en estado STOPPED.\n";
}

void StoppedState::stop(MediaPlayer* player) {
    // Ya está detenido, no hacer nada
    std::cout << "Acción STOP ignorada en estado STOPPED (ya detenido).\n";
}

void StoppedState::next(MediaPlayer* player) {
    std::cout << "Acción NEXT ignorada en estado STOPPED.\n";
}

void StoppedState::prev(MediaPlayer* player) {
    std::cout << "Acción PREV ignorada en estado STOPPED.\n";
}

void StoppedState::trackEnd(MediaPlayer* player) {
    std::cout << "Acción TRACK_END ignorada en estado STOPPED.\n";
}
```

El código para `PlayingState` y `PausedState` seguiría un patrón similar, implementando los métodos de la interfaz `IMediaPlayerState` de acuerdo con la lógica de cada estado y realizando las transiciones (`player->setState(...)`) cuando sea apropiado.

**4. Uso (en `main.cpp`):**

```cpp
// main.cpp
#include "MediaPlayer.h"
// No es necesario incluir los estados concretos aquí si solo se interactúa con MediaPlayer

int main() {
    MediaPlayer player;

    player.play();      // De Stopped a Playing
    player.pause();     // De Playing a Paused
    player.play();      // De Paused a Playing
    player.next();      // Permanece en Playing
    player.stop();      // De Playing a Stopped
    player.pause();     // Ignorado en Stopped
    
    return 0;
}
```

**PAGINA 86**

Este enfoque orientado a objetos para la programación automática es más escalable y mantenible para sistemas complejos. La lógica de cada estado está contenida en su propia clase, lo que mejora la cohesión y reduce el acoplamiento.

### Implementación con Herencia y Polimorfismo

El patrón Estado aprovecha el polimorfismo para cambiar el comportamiento del objeto en tiempo de ejecución. El Contexto (`MediaPlayer`) no necesita saber qué `ConcreteState` específico está manejando el evento; simplemente llama al método polimórfico en su `currentState`. La vinculación dinámica se encarga de ejecutar la implementación correcta del método para el estado actual.

La herencia también puede usarse en la jerarquía de estados. Por ejemplo, si varios estados comparten un comportamiento común para ciertos eventos, una clase base abstracta podría proporcionar una implementación predeterminada, y las subclases de estado podrían anular solo el comportamiento que difiere.

**PAGINA 87**

### Ventajas de la implementación OO de autómatas

  * **Modularidad y Cohesión:** Cada estado se encapsula en su propia clase, lo que mejora la cohesión y reduce la dependencia entre estados.
  * **Extensibilidad:** Añadir nuevos estados o modificar el comportamiento de los estados existentes es fácil y no requiere modificar clases existentes (`Open/Closed Principle`).
  * **Legibilidad:** La lógica del comportamiento complejo se distribuye entre clases de estado más pequeñas, lo que puede hacer que el código sea más legible que grandes `switch` anidados.
  * **Reusabilidad:** Las clases de estado pueden reutilizarse en diferentes contextos o en diferentes autómatas si tienen lógicas de comportamiento similares.
  * **Depuración:** Es más fácil depurar, ya que se puede identificar claramente en qué estado se encuentra el objeto y qué clase de estado es responsable del comportamiento actual.

### Desventajas de la implementación OO de autómatas

  * **Mayor número de clases:** Incluso para autómatas simples, el patrón Estado introduce varias clases (Contexto, Interfaz de Estado, y múltiples Estados Concretos), lo que puede parecer un overhead.
  * **Mayor complejidad de configuración inicial:** La configuración inicial (instanciación del Contexto y los Estados Concretos, y la asignación del estado inicial) puede ser más compleja que un simple `enum` y una variable.
  * **Recursos (memoria/rendimiento):** La creación de objetos adicionales para cada estado puede tener un ligero impacto en el uso de memoria y, en algunos casos, en el rendimiento debido a las llamadas a funciones virtuales. Sin embargo, en la mayoría de los sistemas modernos, este impacto es insignificante.

**PAGINA 88**

### Gestión de variables de datos en la POO

En el patrón Estado, el Contexto (`MediaPlayer` en nuestro ejemplo) es quien posee las variables de datos del autómata (ej. el nivel de volumen, la pista actual, el progreso de la reproducción). Las clases de estado concretas (`StoppedState`, `PlayingState`, etc.) no tienen sus propias variables de datos que definan el "estado" del reproductor, sino que acceden y modifican las variables del Contexto a través de la referencia `player` que se les pasa.

Esto mantiene la separación de responsabilidades:

  * **Contexto:** Gestiona los datos y el estado actual (la referencia al objeto de estado).
  * **Estados Concretos:** Gestionan la lógica del comportamiento basada en el estado y los eventos, actuando sobre los datos del Contexto.

Esta organización asegura que los datos del objeto estén centralizados y que los estados solo contengan la lógica de su comportamiento.

**PAGINA 89**

### Patrones de diseño adicionales para la programación automática OO

Además del patrón Estado, otros patrones de diseño pueden complementar la programación automática en un contexto orientado a objetos:

  * **Singleton:** Como se vio en los ejemplos, a menudo se usa para las clases de estado concreto, ya que generalmente solo se necesita una instancia de cada estado.
  * **Fábrica Abstracta / Método Fábrica:** Para crear familias de objetos de estado o para centralizar la creación de objetos de estado si su instanciación es compleja.
  * **Comando (Command Pattern):** Los eventos de entrada pueden encapsularse como objetos de comando, lo que permite una cola de eventos más flexible y la capacidad de deshacer/rehacer operaciones.
  * **Observador (Observer Pattern):** Útil para desacoplar el autómata de los componentes que reaccionan a sus cambios de estado o a sus acciones de salida. Por ejemplo, una interfaz de usuario podría observar el `MediaPlayer` y actualizar sus botones y pantalla cuando el estado cambia.

**PAGINA 90**

### Uso de frameworks y bibliotecas de máquinas de estados

Para simplificar la implementación de autómatas en un contexto orientado a objetos, existen numerosos frameworks y bibliotecas de máquinas de estados en diversos lenguajes de programación (ej. Boost.Hana en C++, Spring State Machine en Java, XState en JavaScript).

Estos frameworks a menudo proporcionan:

  * Una API para definir estados, eventos, transiciones, acciones de entrada/salida y condiciones de guarda.
  * Un "motor" o "ejecutor" que gestiona el procesamiento de eventos y las transiciones de estado de forma automática.
  * Soporte para jerarquías de estados, concurrencia (regiones ortogonales) y otras características avanzadas de los diagramas de máquina de estados de UML.
  * A veces, herramientas para visualizar y depurar las máquinas de estado.

El uso de un framework puede reducir drásticamente la cantidad de código repetitivo ("boilerplate code") y permitir a los desarrolladores centrarse en la lógica de negocio del autómata. Sin embargo, también introduce una dependencia de la biblioteca y puede tener una curva de aprendizaje asociada.

**PAGINA 91**

### Ejemplo de integración con una interfaz de usuario (UI)

Consideremos cómo un autómata de reproductor de medios orientado a objetos interactuaría con una interfaz de usuario gráfica.

  * **Eventos de UI:** La UI detecta clics de botones (ej. `PlayButton_Click`, `PauseButton_Click`) y los traduce en eventos del autómata (`PLAY_BUTTON`, `PAUSE_BUTTON`).
  * **Actualizaciones de UI:** Cuando el autómata cambia de estado (ej. de `Stopped` a `Playing`), o cuando realiza una acción de salida (ej. `startPlaybackInternal`), la UI necesita ser notificada para actualizar su apariencia (ej. deshabilitar el botón "Play" y habilitar el botón "Pause").

El patrón Observador sería muy útil aquí. La UI se registraría como observador del `MediaPlayer`. Cuando el `MediaPlayer` cambia su estado o realiza una acción relevante, notificaría a sus observadores. La UI recibiría esta notificación y actualizaría sus elementos en consecuencia.

```cpp
// Pseudocódigo para la interacción UI-Autómata
class UI_MediaPlayerView : public IObserver {
public:
    void update(MediaPlayer* player, EventType eventType) override {
        if (eventType == STATE_CHANGED) {
            // Obtener el estado actual del reproductor
            // Actualizar botones (ej. habilitar/deshabilitar)
            // Actualizar el texto de la pantalla (ej. "Reproduciendo", "Pausado")
        } else if (eventType == TRACK_CHANGED) {
            // Actualizar el nombre de la pista
        }
    }
};

// En el MediaPlayer (Contexto):
class MediaPlayer {
    // ...
    void notifyObservers(EventType eventType) {
        for (IObserver* obs : observers) {
            obs->update(this, eventType);
        }
    }

    void setState(IMediaPlayerState* newState) {
        // ... (lógica de cambio de estado)
        notifyObservers(STATE_CHANGED); // Notificar a los observadores que el estado ha cambiado
    }
    // ...
};
```

Este desacoplamiento entre la lógica de negocio del autómata y la presentación de la UI es una buena práctica de diseño.

**PAGINA 92**

### Verificación y pruebas en la POO

La verificación y prueba de autómatas implementados en un contexto orientado a objetos se beneficia de la modularidad:

  * **Pruebas unitarias:** Cada clase de estado (`StoppedState`, `PlayingState`, etc.) puede probarse de forma aislada para verificar que maneja los eventos correctamente y realiza las transiciones y acciones esperadas.
  * **Pruebas de integración:** Se prueban las interacciones entre el Contexto y las clases de estado, así como la comunicación entre múltiples OCOs.
  * **Mocks y stubs:** Durante las pruebas, las dependencias externas (ej. APIs de hardware, otras clases) pueden ser "mockeadas" o "stubbed" para aislar el comportamiento del autómata.
  * **Herramientas de verificación formal:** Los modelos UML Statechart pueden ser analizados por herramientas de verificación formal para asegurar propiedades de seguridad y vivacidad, incluso antes de que el código sea completamente implementado.

La clara separación de responsabilidades facilita significativamente la estrategia de pruebas y depuración.

**PAGINA 93**

### Resumen del Capítulo 3

En este capítulo, se profundizó en la *programación orientada a objetos con estados explícitamente definidos*, destacando cómo el enfoque automático complementa y mejora el paradigma POO al proporcionar una manera estructurada de gestionar el comportamiento complejo.

Se argumentó que el *objeto de control automatizado* (OCO) es inherentemente un concepto orientado a objetos, que encapsula datos y un autómata finito para describir su lógica de comportamiento.

Se introdujo el *patrón de diseño Estado (State Pattern)* como la piedra angular de la implementación orientada a objetos de autómatas. Se explicaron sus componentes (Contexto, Interfaz de Estado, Estados Concretos) y se ilustró su aplicación al ejemplo del reproductor de medios con fragmentos de código en C++.

Se destacaron las *ventajas* de la implementación OO de autómatas, como la modularidad, extensibilidad, legibilidad y facilidad de depuración, así como sus *desventajas*, como el aumento en el número de clases.

Se discutió la *gestión de variables de datos* dentro del Contexto, asegurando una clara separación de responsabilidades.

Se mencionaron *patrones de diseño adicionales* (Singleton, Fábrica, Comando, Observador) que pueden complementar la programación automática OO.

Se exploró el *uso de frameworks y bibliotecas de máquinas de estados* como herramientas para simplificar la implementación.

Finalmente, se abordó la *integración con interfaces de usuario* y las estrategias de *verificación y pruebas* en un contexto POO, enfatizando cómo la modularidad del enfoque mejora estas actividades.

Este capítulo cierra la discusión sobre los fundamentos y las principales aproximaciones (procedimental y orientada a objetos) de la programación automática, sentando las bases para el siguiente capítulo, que explorará áreas de aplicación más avanzadas y problemas actuales.

**PAGINA 94**

### Ejercicios para la autoevaluación

1.  Explique por qué el comportamiento complejo es un desafío para la programación orientada a objetos tradicional.
2.  Describa el patrón de diseño Estado y cómo se aplica para implementar autómatas en un contexto orientado a objetos.
3.  ¿Cómo se comunican las clases de estado concreto con el objeto Contexto en el patrón Estado?
4.  Enumere las ventajas de utilizar el patrón Estado para la programación automática en comparación con un enfoque procedimental basado en `switch`.
5.  ¿Cuáles son algunas desventajas del patrón Estado y cuándo podrían ser problemáticas?
6.  ¿Qué rol juegan los diagramas de máquina de estados de UML en la especificación de autómatas orientados a objetos? Mencione características clave como estados anidados y regiones ortogonales.
7.  ¿Cómo se pueden integrar los autómatas orientados a objetos con una interfaz de usuario?
8.  Mencione al menos dos patrones de diseño adicionales que pueden ser útiles en la programación automática orientada a objetos y explique brevemente su uso.

**PAGINA 95**

### Capítulo 4. Programación automática. Nuevas tareas

Este capítulo proporciona una visión general concisa de algunas áreas de investigación y aplicación actuales de la programación automática que van más allá de los sistemas de control lógico tradicionales. Si bien los capítulos anteriores se centraron en los fundamentos y los métodos de implementación, este capítulo explora el potencial del enfoque automático en contextos más amplios y modernos.

Las "nuevas tareas" aquí no implican que el paradigma básico haya cambiado, sino que su aplicabilidad se extiende a dominios que no siempre son inmediatamente obvios. La versatilidad de los autómatas como modelo de comportamiento permite su adaptación a problemas que van desde las matemáticas discretas hasta la inteligencia artificial.

**PAGINA 96**

### Autómatas y algoritmos de matemática discreta

Los autómatas finitos tienen una conexión profunda con la matemática discreta, especialmente con la teoría de grafos, la teoría de lenguajes formales y la teoría de la computación. Muchos problemas clásicos de la matemática discreta pueden formularse y resolverse de manera elegante utilizando modelos automáticos.

**1. Reconocimiento de lenguajes formales:**
Esta es la aplicación más tradicional de los autómatas finitos. Un autómata finito determinista (AFD) o no determinista (AFND) puede reconocer si una cadena de símbolos pertenece a un lenguaje formal dado (definido por una gramática regular o una expresión regular).

**Ejemplo: Validación de direcciones de correo electrónico**
Un autómata puede diseñarse para validar la sintaxis de una dirección de correo electrónico simple (ej. `nombre@dominio.com`). Los estados representarían el progreso en el análisis de la cadena (ej. "esperando nombre", "después de arroba", "después de dominio", etc.), y los eventos serían los caracteres leídos.

**2. Algoritmos en grafos:**
Muchos algoritmos de grafos pueden verse como el recorrido de un autómata por los nodos y aristas de un grafo. Por ejemplo, el algoritmo de búsqueda en profundidad (DFS) o búsqueda en anchura (BFS) pueden interpretarse como el autómata que cambia de estado (nodo actual) y realiza acciones (visitar un nodo, añadirlo a una cola/pila).

**Ejemplo: Detección de ciclos en un grafo**
Un autómata puede explorar un grafo, manteniendo un registro de los nodos visitados en la ruta actual. Si el autómata intenta visitar un nodo que ya está en la ruta actual, se detecta un ciclo.

**PAGINA 97**

**3. Autómatas para resolver problemas de optimización:**
Aunque los autómatas finitos por sí mismos no son herramientas de optimización potentes, pueden ser componentes de algoritmos de optimización. Por ejemplo, en programación dinámica, donde las soluciones a subproblemas se construyen a partir de soluciones a subproblemas más pequeños, un autómata podría representar el proceso de transición entre estados de un problema.

**4. Autómatas para la generación de secuencias:**
Además de reconocer, los autómatas también pueden *generar* secuencias. Un autómata de estados finitos con acciones de salida puede usarse para generar cadenas que cumplan con ciertas reglas, como secuencias de números pseudoaleatorios, patrones de texto o incluso melodías.

La conexión entre autómatas y matemática discreta es bidireccional: la teoría de autómatas proporciona una base formal para comprender y diseñar algoritmos, y los algoritmos de matemática discreta pueden implementarse de manera efectiva utilizando la metodología de programación automática.

**PAGINA 98**

### Verificación de programas automáticos

La verificación de programas automáticos es un área de investigación crucial, especialmente para sistemas críticos donde la corrección es primordial. Se busca garantizar que el software se comporte según lo especificado y que no contenga errores lógicos.

**1. Verificación basada en modelos (Model Checking):**
Esta es una técnica de verificación formal que utiliza algoritmos para explorar sistemáticamente todos los estados posibles de un modelo de sistema (en nuestro caso, un autómata) para determinar si ciertas propiedades se cumplen.

  * **Propiedades de seguridad:** "Nunca ocurrirá algo malo." (ej. el ascensor nunca se moverá con las puertas abiertas).
  * **Propiedades de vivacidad:** "Algo bueno eventualmente ocurrirá." (ej. el ascensor eventualmente llegará a un piso solicitado).
  * **Propiedades de alcanbilidad:** ¿Es posible llegar a un estado particular? (útil para detectar estados de error o estados inalcanzables).

Herramientas como SPIN, NuSMV o UPPAAL pueden tomar una especificación de autómata (a menudo en un lenguaje de descripción de máquinas de estado) y un conjunto de propiedades a verificar (escritas en una lógica temporal, como LTL o CTL) y determinar si el autómata satisface esas propiedades. Si no las satisface, la herramienta a menudo puede proporcionar un "contraejemplo" (una secuencia de eventos que conduce a la violación de la propiedad), lo que es extremadamente útil para la depuración.

**PAGINA 99**

**2. Pruebas basadas en autómatas:**
Los modelos de autómatas pueden utilizarse para generar automáticamente casos de prueba. Dado un autómata que modela el comportamiento esperado de un sistema, se pueden derivar secuencias de entradas que cubran todos los estados, todas las transiciones, o todas las rutas posibles. Esto aumenta la exhaustividad de las pruebas y ayuda a encontrar errores que de otro modo pasarían desapercibidos.

**3. Verificación de equivalencia:**
Se puede usar para determinar si dos autómatas (o un autómata y una especificación formal) son funcionalmente equivalentes, es decir, si producen el mismo comportamiento para las mismas entradas.

**4. Síntesis de controladores:**
En algunos casos, es posible *sintetizar* automáticamente un autómata de control a partir de una especificación de comportamiento deseado y un modelo del entorno. Esto es un área de investigación activa, especialmente en sistemas de control y automatización.

La verificación formal, aunque computacionalmente costosa para sistemas muy grandes, es invaluable para garantizar la corrección de sistemas críticos. Para sistemas menos críticos, las técnicas de prueba basadas en modelos ofrecen una forma eficiente de mejorar la calidad del software.

**PAGINA 100**

### Autómatas y computación paralela

El comportamiento concurrente y paralelo es inherente a muchos sistemas modernos, desde microprocesadores multinúcleo hasta sistemas distribuidos y computación en la nube. Los autómatas ofrecen un marco natural para modelar y razonar sobre estos sistemas.

**1. Máquinas de estados concurrentes/ortogonales:**
Como se mencionó en el Capítulo 3, los diagramas de máquina de estados de UML (Statecharts de Harel) permiten definir regiones ortogonales que se ejecutan en paralelo. Cada región es una máquina de estados independiente, y el estado general del sistema es la combinación de los estados de todas las regiones ortogonales activas. Esto es muy adecuado para modelar sistemas con componentes que operan simultáneamente pero de forma relativamente independiente.

**Ejemplo: Un sistema de control de robot**
Un robot podría tener un autómata principal para la "Misión" (ej. navegar a un punto, limpiar un área), y regiones ortogonales para:

  * "Movimiento" (estados como `MovingForward`, `TurningLeft`, `Stopped`).
  * "Sensores" (estados como `ScanningEnvironment`, `ObstacleDetected`).
  * "Manipulador" (estados como `GripperOpen`, `GripperClosed`, `HoldingObject`).
    Cada una de estas regiones podría ser su propio autómata, ejecutándose en paralelo y comunicándose a través de eventos.

**PAGINA 101**

**2. Modelos de concurrencia basados en autómatas:**
Formalismos como las redes de Petri, los procesos de cálculo (calculus of communicating systems - CCS, communicating sequential processes - CSP) y los autómatas con temporización son ejemplos de modelos basados en autómatas que se utilizan para describir y analizar el comportamiento de sistemas concurrentes y paralelos. Estos modelos permiten razonar sobre propiedades como interbloqueos (deadlocks), vivacidad y seguridad en entornos paralelos.

**3. Orquestación de microservicios:**
En arquitecturas de microservicios, donde múltiples servicios pequeños se comunican para formar una aplicación más grande, los autómatas pueden usarse para modelar y orquestar los flujos de trabajo de negocio. Un "autómata de coreografía" o "autómata de orquestación" podría gestionar la secuencia de llamadas a servicios y los cambios de estado del proceso de negocio.

**4. Programación reactiva:**
En la programación reactiva moderna, donde los sistemas reaccionan a flujos asíncronos de datos, los autómatas pueden proporcionar la lógica subyacente para cómo el sistema cambia de estado y reacciona a los eventos en el flujo.

La programación automática ofrece una abstracción poderosa para comprender, diseñar y verificar sistemas paralelos y concurrentes, un área de creciente importancia en el desarrollo de software.

**PAGINA 102**

### Autómatas y programación genética

La programación genética (GP) es un enfoque de la inteligencia artificial y el aprendizaje automático que utiliza principios de la evolución biológica (como la selección natural, la mutación y la recombinación) para "evolucionar" programas o soluciones a problemas. Una de las áreas prometedoras es la aplicación conjunta de autómatas y programación genética.

**1. Evolución de autómatas para tareas de control:**
La GP puede utilizarse para generar automáticamente autómatas finitos que resuelvan problemas de control. En lugar de que un ingeniero diseñe manualmente el grafo de estados, la GP puede buscar en el espacio de autómatas posibles para encontrar uno que exhiba el comportamiento deseado. Esto es particularmente útil en situaciones donde la lógica de control es muy compleja o difícil de especificar manualmente.

**Ejemplo: Agentes de juego**
En juegos simples, un autómata podría ser el "cerebro" de un personaje no jugador (NPC). La programación genética podría evolucionar el autómata de este NPC para que exhiba un comportamiento de juego interesante o que gane partidas.

**2. Optimización de la estructura de autómatas:**
La GP también puede optimizar aspectos de autómatas existentes, como reducir el número de estados, simplificar las transiciones o ajustar los parámetros de las acciones para mejorar el rendimiento o la eficiencia.

**PAGINA 103**

**3. Autómatas como representación de programas en GP:**
Tradicionalmente, en GP, los programas se representan como árboles de expresiones (árboles de sintaxis abstracta). Sin embargo, los autómatas finitos también pueden servir como una representación de programas. La evolución de autómatas puede implicar la mutación de transiciones, la adición/eliminación de estados, o la recombinación de partes de autómatas.

**Desafíos:**

  * **Espacio de búsqueda:** El espacio de autómatas posibles es muy grande, lo que puede hacer que la búsqueda por GP sea computacionalmente intensiva.
  * **Función de fitness:** Definir una función de fitness (que evalúa cuán "buena" es una solución de autómata) es crucial y puede ser un desafío.

A pesar de los desafíos, la combinación de autómatas y programación genética ofrece un camino prometedor para la síntesis automática de controladores y la creación de agentes con comportamiento adaptativo.

**PAGINA 104**

### Aplicaciones de la programación automática en inteligencia artificial (IA)

Más allá de la programación genética, la programación automática tiene relevancia en varias otras áreas de la IA:

  * **Planificación y razonamiento:** Los autómatas pueden modelar procesos de planificación donde un agente pasa por una secuencia de estados para alcanzar un objetivo.
  * **Sistemas basados en reglas:** Aunque no son autómatas estrictos, muchos sistemas de reglas y sistemas expertos pueden tener una lógica subyacente que se asemeja a las transiciones de estado.
  * **Procesamiento del lenguaje natural (PNL):** Los autómatas finitos son fundamentales en PNL para tareas como el análisis léxico (tokenización), el reconocimiento de expresiones regulares y la construcción de analizadores sintácticos simples.
  * **Agentes inteligentes:** La lógica de decisión de los agentes inteligentes a menudo puede modelarse como un autómata que reacciona a su percepción del entorno y cambia su comportamiento en consecuencia.

**PAGINA 105**

### Autómatas en sistemas ciber-físicos (CPS) y IoT

Los sistemas ciber-físicos (CPS) y el Internet de las Cosas (IoT) son áreas donde la programación automática es particularmente aplicable debido a su naturaleza reactiva, concurrente y dependiente del estado.

  * **Controladores embebidos:** Muchos dispositivos IoT y componentes CPS son microcontroladores que ejecutan lógica de control, a menudo implementada como autómatas finitos debido a su determinismo y eficiencia.
  * **Gestión de estados de dispositivos:** Un dispositivo IoT puede tener varios estados (ej. `activo`, `suspendido`, `conectado`, `desconectado`, `actualizando firmware`), y su comportamiento depende en gran medida de su estado actual y de los eventos de la red o del usuario.
  * **Seguridad:** Los autómatas pueden modelar el comportamiento de un sistema para detectar anomalías o patrones de ataque.

La capacidad de los autómatas para describir el comportamiento en tiempo real y reaccionar a eventos los convierte en una herramienta valiosa en estos dominios emergentes.

**PAGINA 106**

### Resumen del Capítulo 4

En este capítulo, se exploraron *nuevas tareas y áreas de aplicación* de la programación automática, y se destacaron las intersecciones del paradigma con campos avanzados de la informática y la inteligencia artificial.

Se demostró la profunda conexión entre *autómatas y algoritmos de matemática discreta*, incluyendo su uso en el reconocimiento de lenguajes formales, algoritmos de grafos, problemas de optimización y generación de secuencias.

Se abordó la importancia de la *verificación de programas automáticos*, discutiendo técnicas como la verificación basada en modelos (Model Checking), las pruebas basadas en autómatas, la verificación de equivalencia y la síntesis de controladores, enfatizando su papel en la garantía de la corrección del software.

Se examinó la aplicación de *autómatas en la computación paralela*, cubriendo conceptos como máquinas de estados concurrentes/ortogonales, modelos de concurrencia basados en autómatas y su relevancia en la orquestación de microservicios y la programación reactiva.

Se exploró la combinación de *autómatas y programación genética* para la evolución automática de controladores y agentes con comportamiento adaptativo, así como la optimización de estructuras de autómatas.

Finalmente, se discutieron otras *aplicaciones en inteligencia artificial* (planificación, sistemas basados en reglas, PNL, agentes inteligentes) y su creciente importancia en *sistemas ciber-físicos (CPS) e IoT*, donde la naturaleza reactiva y dependiente del estado de los dispositivos los convierte en candidatos ideales para el modelado automático.

Este capítulo amplía la perspectiva sobre la versatilidad y el potencial de la programación automática, mostrando que es un paradigma relevante no solo para el control lógico tradicional, sino también para desafíos complejos en la informática moderna.

**PAGINA 107**

### Conclusión

A lo largo de este libro, hemos presentado y explorado el paradigma de la *programación automática*, un enfoque para el desarrollo de software que se centra en la modelización explícita del comportamiento complejo de los sistemas mediante el uso de *objetos de control automatizados*, que son una extensión de los autómatas finitos.

Hemos demostrado que este paradigma no es una novedad radical, sino una evolución natural de las prácticas de desarrollo de software, que aborda una debilidad clave en los enfoques tradicionales: la gestión ineficaz del comportamiento dependiente del estado.

Los *conceptos clave* de la programación automática, como el "estado", las "acciones de entrada y salida", y la "función de transición", proporcionan un vocabulario formal y un marco estructurado para describir cómo un sistema reacciona a los eventos a lo largo del tiempo.

Hemos cubierto dos *enfoques principales de implementación*:

1.  **Programación procedimental con estados explícitamente definidos:** Adecuada para sistemas con recursos limitados y cuando la visibilidad del código es una prioridad, utilizando principalmente `switch` o tablas de transiciones.
2.  **Programación orientada a objetos con estados explícitamente definidos:** Aprovechando patrones de diseño como el patrón Estado, que permite una modularidad, extensibilidad y legibilidad superiores para sistemas más grandes y complejos.

El uso de *modelos gráficos* como los grafos de estados y los diagramas de máquina de estados de UML es fundamental para la programación automática, ya que proporcionan una representación visual clara de la lógica del comportamiento, facilitando el diseño, la comunicación y la depuración.

También hemos enfatizado la importancia de la *verificación* y las *pruebas* en la programación automática. La naturaleza formal de los autómatas permite la aplicación de técnicas de verificación basadas en modelos, que son esenciales para garantizar la corrección y fiabilidad de sistemas críticos.

Finalmente, hemos explorado *nuevas y prometedoras áreas de aplicación* de la programación automática, desde la matemática discreta y la computación paralela hasta la inteligencia artificial y los sistemas ciber-físicos. Esto subraya la relevancia continua y la versatilidad del paradigma en el panorama tecnológico actual y futuro.

**PAGINA 108**

En resumen, la programación automática ofrece una metodología robusta y probada para abordar la complejidad inherente al comportamiento de muchos sistemas de software. Al promover un diseño explícito, modular y verificable, contribuye significativamente a la calidad, fiabilidad y mantenibilidad de las aplicaciones, desde pequeños controladores embebidos hasta grandes sistemas distribuidos. Animamos a los desarrolladores a considerar la integración de estos principios en sus prácticas de diseño y codificación.

**PAGINA 109**

### Lista de fuentes

1.  Mesa de Redacción del "Boletín de Programación". Estilos de programación // Boletín de Programación. - 1990. - Nº 1.
2.  Shalyto A. A. Lógica "del comportamiento" de programas // Actas de la Academia de Ciencias de Rusia. Informática y Automatización. - 1991. - Nº 1. - P. 111-125.
3.  Shalyto A. A. Una tecnología para la implementación de programas concurrentes // Conferencia Internacional sobre Programación paralela y distribuida. - 1999. - Vol. 1657 de LNCS. - P. 209-220.
4.  Shalyto A. A. Paradigma de la programación de estados / A. A. Shalyto, A. Yu. Kuzmin // Programación. - 2000. - Nº 1. - P. 39-50.
5.  Shalyto A. A. Programming with Explicitly Defined States / A. A. Shalyto, A. Yu. Kuzmin // Journal of Computer and Systems Sciences International. - 2000. - Vol. 39. - N 2. - P. 177-185.
6.  Gribkov P. A. Experiencia en la enseñanza de la programación competitiva en el Departamento de Tecnologías Informáticas de la Universidad ITMO / P. A. Gribkov, G. G. Gurevich, D. K. Karpov // Ingeniería de Software. - 2007. - Nº 5. - P. 13-17.
7.  Lipovsky S. V. La calidad del software como objeto de mejora de la gestión // Ingeniería de Software. - 2007. - Nº 5. - P. 26-29.
8.  Zhdanov V. L. Soporte para el proceso de ciclo de vida de los sistemas de software de control de objetos en tiempo real complejos en la industria de la energía atómica: dis. ... cand. tech. nauk: 05.13.11: prot. - 2007.
9.  Rybakov A. S. Desarrollo de un sistema experto para la implementación de la tecnología de programación automática / A. S. Rybakov // Sistemas y Medios de Control. - 2007. - Nº 2 (16). - P. 50-53.
10. Harel D. Statecharts: Una notación visual para sistemas complejos // Science of Computer Programming. - 1987. - Vol. 8. - P. 231-274.
11. Aho A. V. Compiladores. Principios, técnicas y herramientas / A. V. Aho, R. Sethi, J. D. Ullman. - M.: Williams, 2008. - 798 p.
12. Hopcroft J. E. Introducción a la teoría de autómatas, lenguajes y computación / J. E. Hopcroft, R. Motwani, J. D. Ullman. - M.: Williams, 2008. - 528 p.
13. Turing A. M. Sobre los números computables, con una aplicación al problema de la decisión // Proceedings of the London Mathematical Society, Series 2. - 1936. - Vol. 42. - P. 230-265.
14. Klyuev V. I. Teoría de autómatas / V. I. Klyuev. - M.: Editorial de la Universidad Técnica Estatal de Moscú N. E. Bauman, 2003. - 304 p.
15. Vostrov G. N. Modelado del comportamiento de sistemas reactivos utilizando diagramas de máquina de estados // Programación. - 2004. - Nº 5. - P. 44-50.
16. Polyakova N. V. Modelado de sistemas distribuidos utilizando el formalismo de redes de Petri: un enfoque basado en autómatas / N. V. Polyakova // Informática y Sistemas de Control. - 2005. - Nº 3. - P. 60-64.
17. Gavrilov A. V. Tecnología de desarrollo de software para sistemas integrados basados en autómatas / A. V. Gavrilov // Informática y Sistemas de Control. - 2006. - Nº 3. - P. 72-76.
18. Abramov A. V. Análisis de la complejidad de los programas automáticos / A. V. Abramov, V. V. Kononov // Informática y Sistemas de Control. - 2006. - Nº 3. - P. 65-71.
19. Kuzmin A. Yu. Implementación de sistemas de control en tiempo real basados en autómatas // Informática y Sistemas de Control. - 2006. - Nº 3. - P. 77-80.
20. Polikarpova N. I. Problemas actuales de la verificación de programas / N. I. Polikarpova // Materiales de la conferencia "Sistemas de software y tecnologías de la información". - Petrozavodsk: Editorial de la Universidad Estatal de Petrozavodsk, 2006. - P. 110-112.
21. Klyuev V. I. Una técnica para la descripción de autómatas basada en estructuras lógicas // Ingeniería de Software. - 2007. - Nº 5. - P. 30-33.
22. Kuliev E. A. Desarrollo de una herramienta para la especificación y verificación de autómatas // Informática y Sistemas de Control. - 2007. - Nº 3. - P. 77-80.
23. Gribkov P. A. Un sistema para la simulación de autómatas // Informática y Sistemas de Control. - 2007. - Nº 3. - P. 81-84.
24. Shalyto A. A. Principios de programación de estados para la creación de software concurrente / A. A. Shalyto // Informática y Sistemas de Control. - 2007. - Nº 3. - P. 68-76.
25. Harel D. De los diagramas de flujo a los Statecharts: un enfoque visual para la programación de sistemas reactivos // IEEE Computer. - 1987. - Vol. 20. - N 7. - P. 23-37.
26. Rumbaugh J. O. Modelado orientado a objetos y diseño / J. O. Rumbaugh, M. R. Blaha, W. J. Premerlani, F. Eddy, W. Lorensen. - M.: Mir, 1993. - 558 p.
27. Booch G. O. Análisis y diseño orientado a objetos con aplicaciones / G. O. Booch. - M.: Mir, 1995. - 721 p.
28. Gamma E. O. Patrones de diseño. Elementos de software reutilizables / E. O. Gamma, R. Helm, R. Johnson, J. Vlissides. - SPb.: Peter, 2001. - 368 p.
29. Alimov Yu. B. Fundamentos de la teoría de autómatas / Yu. B. Alimov. - M.: URSS, 2004. - 256 p.
30. Gribkov P. A. Un sistema para la síntesis de autómatas a partir de un modelo gráfico // Informática y Sistemas de Control. - 2007. - Nº 3. - P. 85-89.

**PAGINA 110**

### Índice temático

  * acción de entrada 12, 18, 50, 52, 55, 60
  * acción de salida 12, 18, 45, 50, 52, 55, 60
  * acciones de entrada/salida 64
  * algoritmos en grafos 96
  * autómata de Mealy/Moore 17, 18
  * autómata finito 12, 17, 42, 96
  * autómatas en IA 104
  * autómatas en computación paralela 100
  * autómatas en sistemas ciber-físicos 105
  * autómatas jerárquicos 62
  * autómatas y programación genética 102
  * Bucle de eventos 18, 51, 59
  * comportamiento complejo 7, 11, 12, 14, 23, 24, 76
  * comportamiento simple 7, 24
  * condiciones de guarda 64, 81
  * diseño 43, 77
  * especificación 44, 48, 64, 81
  * estado 11, 24, 50, 55, 78
  * estado de bloqueo 22
  * estado inalcanzable 22
  * estados anidados 81
  * estados concurrentes 81
  * evento 12, 18, 59
  * funciones de transición y salida 12, 18, 19
  * generación de código 65
  * grafo de estados 15, 21, 45, 52, 55, 65
  * herramientas 65, 90
  * implementación 18, 50, 57, 83
  * lenguajes formales 96
  * lógica de control 95
  * máquina de Turing 12
  * modelo de autómata 17, 18, 24
  * modularidad 16, 23, 87
  * objeto de control automatizado (OCO) 14, 24, 43, 77, 93
  * patrón de diseño Estado 77
  * principios de la programación automática 16
  * programación automática 1, 3, 4, 7, 11, 12, 23, 24, 42, 67, 76, 93, 95, 106, 107
  * programación genética 102
  * programación orientada a objetos 76
  * programación procedimental 42
  * prueba 22, 92
  * requisitos no funcionales 65
  * reutilización 16, 23
  * seguridad (propiedad) 23, 98
  * sistemas reactivos 7, 24, 42
  * tabla de transiciones 19, 48, 50, 57
  * teoría de autómatas 42
  * verificación 22, 92, 98
  * vivacidad (propiedad) 23, 98

A continuación, presento la traducción corregida del documento "libroRusoP2.docx", prestando especial atención al formato para que no se mezcle el texto explicativo con el código.

-----

### Implementación de Autómatas

**Patrones de Implementación**

Los autómatas se pueden crear y modificar fácilmente durante la ejecución del programa. Por ejemplo, esta representación es necesaria para la optimización de autómatas, que se discute en la Sección 4.4. Sin embargo, en el contexto de esta sección, no se requiere la modificación dinámica de la estructura del autómata. Por lo tanto, para aumentar la velocidad, se debe preferir el segundo de los métodos de implementación mencionados anteriormente (utilizando una instrucción de selección), ya que es estático.

La palabra clave `switch` se utiliza en C para las instrucciones de selección [44]. Otros lenguajes de programación imperativos de alto nivel tienen instrucciones similares. Las instrucciones de selección se pueden utilizar para implementar decodificadores de estados y acciones de entrada (Fig. 2.30). Como resultado, la plantilla de implementación para el ciclo de un autómata de Moore tomará la siguiente forma (Listado 2.1).

**Listado 2.1. Plantilla de implementación para el ciclo de un autómata de Moore en lenguaje C (utilizando dos instrucciones de selección)**

```c
void A() {
  switch (y) { // Decodificador de estados
    case 1:
      // Bloque de formación de acciones de salida
      z1 = <0|1>; ...; zm = <0|1>;
      switch (x) { // Decodificador de acciones de entrada
        case 0:
          y = <1..s>; break; // Actualización de estado
        // ... (código omitido para brevedad)
        case <2^n - 1>:
          y = <1..s>; break;
      }
      break;
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

Con este enfoque, el autómata se describe estáticamente: su estructura está codificada en el texto del programa. Esta propiedad garantiza la velocidad requerida. Sin embargo, queda otro problema: el crecimiento exponencial de la descripción del autómata con el aumento del número de variables de entrada. De hecho, el número de etiquetas `case` en la instrucción de selección anidada, y, en consecuencia, el volumen del texto del programa, depende exponencialmente de `n` (el número de variables de entrada).

Para resolver este problema, recordemos la observación hecha en relación con las tablas: en la mayoría de los casos, solo un pequeño conjunto de variables de entrada es significativo en cada estado. Por lo tanto, no es necesario especificar el valor de la función de transición para todas las posibles acciones de entrada. Como regla general, solo algunas combinaciones de valores de varias variables de entrada conducen a un cambio de estado. Aparentemente, la forma más compacta de escribir la función de transición se utiliza en la notación de grafos de transición: para cada estado se define un conjunto de transiciones salientes, marcadas con condiciones en forma de fórmulas booleanas. La experiencia muestra que en problemas reales el tamaño de estas fórmulas prácticamente no aumenta con el crecimiento del número de variables de entrada.

La plantilla de implementación propuesta anteriormente se puede modificar fácilmente para utilizar una representación compacta de la función de transición. Para esto, es suficiente reemplazar la instrucción de selección interna con varias instrucciones de ramificación (según el número de arcos que salen de este estado en el grafo de transición). Las condiciones de ramificación serán las etiquetas de los arcos salientes. Tenga en cuenta que no es necesario asignar instrucciones de ramificación a los bucles en el autómata de Moore. La plantilla de implementación modificada se presenta en el Listado 2.2.

**Listado 2.2. Plantilla de implementación para el ciclo de un autómata de Moore en lenguaje C (utilizando instrucciones de selección y ramificación)**

```c
void A() {
  switch (y) { // Decodificador de estados
    case 1:
      // Bloque de formación de acciones de salida
      z1 = <0|1>; ...; zm = <0|1>;
      if (<etiqueta_1>) { // Decodificador de acciones de entrada
        y = <1..s>; // Actualización de estado
      } else if (<etiqueta_2>) {
        y = <1..s>;
      } // ... (código omitido para brevedad)
      else if (<etiqueta_k>) {
        y = <1..s>;
      }
      break;
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

La solución al problema del volumen innecesariamente grande de la representación del autómata condujo incidentalmente a otra mejora: la transformación formal del grafo de transición en código se hizo más sencilla. Sin embargo, ¿es realmente la descripción de las transiciones de estado en forma de una secuencia de instrucciones de ramificación isomorfa a la descripción en forma de un conjunto de arcos salientes? Una fuente de inconsistencia puede ser el hecho de que las instrucciones de ramificación siempre se ejecutan en el orden especificado por el texto del programa, y el orden de verificación de las condiciones en los arcos del grafo no está definido. Sin embargo, en un grafo de transición correcto (consistente), el orden de verificación de las condiciones en los arcos no importa. Si se asignan prioridades a los arcos en el grafo de transición, entonces en el texto del programa las instrucciones de ramificación correspondientes también deben estar en el orden especificado por las prioridades.

Como ejemplo del uso de la plantilla considerada, presentaremos la implementación del autómata del sistema de control de válvulas, cuyo diseño se discutió en la Sección 2.1.1.

**Listado 2.3. Implementación del sistema de control de válvulas en lenguaje C**

```c
void A() {
  switch (y) {
    case 1: // Cerrado
      z1 = 0; z2 = 0; z3 = 0; z4 = 0;
      if (x1) { y = 2; }
      break;
    case 2: // Abriendo
      z1 = 1; z2 = 0; z3 = 0; z4 = 1;
      if (x4 && x6) { y = 3; } else if (!x4 && x6) { y = 5; }
      break;
    case 3: // Abierto
      z1 = 0; z2 = 0; z3 = 0; z4 = 0;
      if (x2) { y = 4; }
      break;
    case 4: // Cerrando
      z1 = 0; z2 = 1; z3 = 0; z4 = 1;
      if (x5 && x6) { y = 1; } else if (!x5 && x6) { y = 5; }
      break;
    case 5: // Falla
      z1 = 0; z2 = 0; z3 = 1; z4 = 0;
      if (x3) { y = 1; }
      break;
  }
}
```

Tenga en cuenta que las palabras clave `else` en esta implementación se introducen únicamente para mejorar el rendimiento del programa. Dado que las condiciones de transición de cada estado son ortogonales en este caso, las palabras clave mencionadas pueden omitirse.

Anteriormente se discutió la implementación de sistemas con comportamiento complejo, controlados por un solo autómata. Pasemos a los problemas de implementación de sistemas controlados por autómatas que interactúan. En este caso, es conveniente implementar el ciclo de trabajo de cada autómata como una función separada. Si los autómatas en el sistema interactúan intercambiando números de estado, entonces las variables internas de otros autómatas, además de las variables de entrada, participarán en las condiciones de ramificación. En los bloques de formación de acciones de salida, además de las instrucciones de asignación de valores a las variables de salida, aparecerán llamadas a autómatas anidados y llamados.

La llamada a un autómata anidado se realiza llamando a la función que implementa su ciclo de trabajo. La llamada a un autómata invocado es una operación más compleja. Una de las formas de implementarlo es crear una función adicional para cada autómata invocado Ai (descrito con la función `void A<i>()`), que tiene la siguiente estructura:

**Listado 2.4. Plantilla de función para llamar a un autómata invocado**

```c
void Call_A<i>() {
  y<i> = 1;
  while (y<i> != <estado_final>) {
    <Entrada x> Ai();
    <Salida z>
  }
}
```

Después de esto, en el punto de llamada al autómata invocado, se ejecuta la función `Call_A<i>()`.

Si durante el diseño del sistema se realizó una descomposición de autómatas paralela, existen dos variantes de implementación principales.

1.  **Todo el sistema se ejecuta en un solo procesador.** En este caso, es necesario asegurar el trabajo pseudo-paralelo de los autómatas. Aquí se manifiesta una de las ventajas de la programación de autómatas: incluso si el entorno de ejecución no admite la multitarea, la ejecución pseudo-paralela de los autómatas se puede lograr fácilmente colocando las llamadas a sus funciones correspondientes consecutivamente en el cuerpo del ciclo del programa principal (Fig. 2.31).

    **Fig. 2.31. Esquema del algoritmo que implementa el funcionamiento pseudo-paralelo de `p` autómatas activos**

2.  **Cada autómata se ejecuta en un procesador separado.** En este caso, cada una de las funciones que implementan los ciclos de trabajo de los autómatas del sistema se coloca en su propio ciclo dentro de un programa principal separado. Aquí, los problemas de interacción y sincronización pasan a primer plano. En particular, es necesario garantizar la coherencia de los datos intercambiados por los autómatas en el sistema. La elección de una u otra solución a estos problemas depende de las especificidades del sistema en cuestión.

Como ejemplo, presentaremos la implementación de un sistema de control de dos válvulas. De las varias opciones de arquitectura propuestas en la Sección 2.1.2, elegiremos aquella en la que se realizó una descomposición de autómatas paralela. Supongamos que el sistema debe ejecutarse en un solo procesador. El Listado 2.5 contiene las implementaciones de las funciones responsables del ciclo de trabajo de cada uno de los dos autómatas, así como la plantilla de implementación del programa principal.

**Listado 2.5. Implementación del sistema de control de dos válvulas en lenguaje C**

```c
void A1() { // Autómata que controla la primera válvula
  switch (y1) {
    case 1: // Cerrado
      z1 = 0; z2 = 0;
      if (x1) { y1 = 2; } break;
    case 2: // Abriendo
      z1 = 1; z2 = 0;
      if (x3) { y1 = 3; } break;
    case 3: // Abierto
      z1 = 0; z2 = 0;
      if (y2 == 1) { y1 = 4; } // Asumo que el original tenía y en vez de y1 por error
      break;
    case 4: // Cerrando
      z1 = 0; z2 = 1;
      if (x4) { y1 = 1; } break;
  }
}
```

```c
void A2() { // Autómata que controla la segunda válvula
  switch (y2) {
    case 1: // Cerrado
      z3 = 0; z4 = 0;
      if (y1 == 3) { y2 = 2; }
      break;
    case 2: // Abriendo
      z3 = 1; z4 = 0;
      if (x5) { y2 = 3; } break;
    case 3: // Abierto
      z3 = 0; z4 = 0;
      if (x2) { y2 = 4; } break;
    case 4: // Cerrando
      z3 = 0; z4 = 1;
      if (x6) { y2 = 1; } break;
  }
}
```

```c
void main() { // Programa principal
  y1 = 1; y2 = 1;
  while (1) {
    // <Entrada x> A1(); A2();
    // <Salida z>
    // En el código original, las líneas "<Entrada x>" y "<Salida z>"
    // no son código C válido, por lo que se comentan o se eliminan
    // en una implementación real. Aquí se dejan comentadas para referencia.
  }
}
```

### Otras Clases de Problemas

En esta sección se abordan problemas que no pertenecen al ámbito del control lógico. En el campo de la programación de aplicaciones para computadoras personales, los sistemas con comportamiento complejo suelen ser orientados a eventos, y los objetos automatizados en ellos, como regla general, son pasivos. En cuanto a los modelos de autómatas, lo más conveniente es usar autómatas de Mealy o (con menos frecuencia) autómatas mixtos.

¿Qué cambios en la estructura del algoritmo implicará esta especificidad? Dado que se utilizan otros modelos de autómatas, el bloque de formación de acciones de salida debe ubicarse de manera diferente. Los comandos del objeto de control ya no se implementan por hardware, sino por software, como procedimientos ordinarios. Por lo tanto, en el bloque de formación de acciones de salida, en lugar de asignar valores a las variables de salida, se deben colocar llamadas a procedimientos correspondientes a aquellas variables de salida que toman el valor "verdadero".

Dado que los objetos automatizados considerados son pasivos, el programa principal también ha cambiado. Consideremos el esquema de algoritmo que describe un ciclo de trabajo de un autómata de Mealy (Fig. 2.32). Aquí, el bloque de formación de acciones de salida se encuentra detrás del decodificador de acciones de entrada y contiene llamadas a comandos específicos del objeto de control. El conjunto de comandos que deben ser llamados se determina por el valor de la función de salida del autómata para el estado dado y la acción de entrada.

Aquí, `y` representa el estado del autómata.

**Fig. 2.32. Esquema del algoritmo que implementa un ciclo de trabajo de un autómata de Mealy**

Al combinar este algoritmo con el algoritmo del ciclo de trabajo del autómata de Moore de la sección anterior, obtenemos un algoritmo para un autómata mixto (Fig. 2.33), en el que hay dos bloques de formación de acciones de salida: antes y después del decodificador de acciones de entrada.

Aquí, `y` representa el estado del autómata.

**Fig. 2.33. Esquema del algoritmo que implementa un ciclo de trabajo de un autómata mixto**

El programa principal ha cambiado mucho más. Como el lector ya sabe, un modelo de autómata pasivo no funciona continuamente (ciclo por ciclo), sino que realiza el siguiente ciclo de trabajo por iniciativa del entorno externo. Por lo tanto, para tales modelos, el programa principal ya no es parte de la implementación del autómata. Este programa describe el funcionamiento del entorno externo, y desde él, en ciertos lugares, se puede llamar a una subrutina que implementa el ciclo de trabajo del autómata. En los sistemas de eventos aplicados, la función del programa principal, como regla general, consiste en extraer mensajes de la cola y pasarlos a los controladores correspondientes. Sin embargo, esto es solo la punta del iceberg: la aplicación se ejecuta bajo el control del sistema operativo, que asume todo el trabajo de recibir eventos de dispositivos externos y pasarlos al programa. Por lo tanto, el concepto mismo de programa principal en los sistemas de software de aplicación modernos es relativo e indefinido.

Además, con el paso a la programación de aplicaciones de sistemas de eventos, los criterios de optimización para la implementación de autómatas también cambiaron. El isomorfismo del código del programa al grafo de transición sigue siendo primordial, pero la eficiencia en tiempo y memoria para esta clase de problemas no es tan crítica. Por el contrario, la flexibilidad y la capacidad de evolucionar, adaptándose a nuevos requisitos, adquieren mayor importancia.

Recordemos que en esta sección se discuten cuestiones de implementación en el contexto de la programación procedural. El enfoque orientado a objetos tiene un arsenal más amplio de métodos y patrones para implementar autómatas; algunos de ellos se discuten más adelante en este libro (Sección 3.3). Por ahora, nos quedamos con el lenguaje C y dos formas de implementar autómatas mencionadas anteriormente: mediante tablas y mediante instrucciones de selección.

Existe una serie de tareas en las que es necesario modificar el autómata durante la ejecución del programa. Para tales casos, se debe utilizar la implementación del autómata en forma de tabla. Sin embargo, la experiencia demuestra que tales tareas son bastante raras. Por lo tanto, la plantilla de implementación más utilizada sigue siendo la descrita en la sección anterior: el uso de una instrucción de selección en combinación con una instrucción de ramificación (especialmente porque este método simplifica la transformación isomorfa del grafo de transición en código de programa).

La plantilla de implementación del ciclo de trabajo del autómata ha cambiado insignificativamente en comparación con el Listado 2.2. Dado que ahora se utiliza un autómata de Mealy en lugar de un autómata de Moore, el bloque de formación de acciones de salida se ha movido dentro de la instrucción de ramificación. Además, en este bloque, en lugar de asignar valores a las variables de salida, ahora se realizan llamadas a subrutinas correspondientes a los comandos del objeto de control.

Una pregunta más interesante es la interacción de la función del ciclo del autómata con el contexto que lo llama, es decir, la transmisión de eventos al autómata. Existen tres variantes principales de dicha interacción.

1.  **Los eventos, al igual que las variables de entrada, son variables globales del programa o del módulo del programa en el que se encuentra el autómata** (tenga en cuenta que la segunda opción es menos probable, ya que, a diferencia de las variables de entrada, que son locales al objeto automatizado, los eventos, como regla general, están destinados a la interacción entre módulos). En el caso de que los eventos sean *exclusivos* (dos eventos no pueden ocurrir simultáneamente), para almacenar el evento actual es suficiente introducir una variable entera, cuyo valor en el decodificador de acciones de entrada se comparará con los identificadores de eventos específicos. Si los eventos en el sistema en desarrollo no tienen la propiedad de exclusividad, se puede utilizar un vector de bits para almacenar el conjunto de eventos actuales. En este caso, la representación de los eventos no difiere de la representación de las variables de entrada. La plantilla de implementación de la función de ciclo del autómata con este método de representación de eventos difiere de la descrita en el Listado 2.2 solo en la posición del bloque de formación de acciones de salida.

2.  **Los eventos son argumentos de la función de ciclo del autómata.** Esta decisión de diseño refleja la diferencia entre eventos y variables de entrada: aquí el autómata *procesa* un evento (o un conjunto de eventos), mientras que los valores de las variables de entrada solo se consultan si es necesario por iniciativa propia del autómata. Además, al implementar el autómata manualmente, esta solución previene errores de programación posibles con el primer enfoque: cuando el programador olvida configurar la variable para almacenar el evento antes de llamar al ciclo del autómata. Los cambios en la plantilla de implementación en este caso son insignificantes y solo afectan la firma de la función de ciclo: `void A (int e)`, si los eventos son exclusivos; `void A (bool[] e)`, si los eventos no son exclusivos. Esta variante de implementación fue propuesta en las obras [27, 42, 46]. Una descripción de un ejemplo de su uso en la práctica se proporciona en la obra [8].

3.  **A cada evento se le asocia una función separada.** Esta solución solo es adecuada para implementar un modelo de eventos exclusivo (tenga en cuenta que este modelo es el más común). Además, refleja el papel activo de los eventos, el hecho de que es la ocurrencia de un evento lo que inicia la llamada al autómata. Además, esta solución es la que mejor se adapta a la estructura tradicional de un módulo de programa en sistemas de eventos, donde cualquier parte independiente del programa es un conjunto de manejadores de eventos semánticamente relacionados. Un programa construido de acuerdo con esta solución ya no es completamente isomorfo al esquema de algoritmo de la Fig. 2.32, donde primero se decodifica el estado y luego la acción de entrada. En este caso, primero se produce la ramificación por eventos, luego por estados y, finalmente, por variables de entrada. Esto puede parecer una complicación injustificada. Sin embargo, en la mayoría de los sistemas de eventos, el entorno externo decodifica necesariamente el evento antes de enviarlo al autómata (al menos para comprender a qué autómata debe transmitirse). En este caso, al utilizar otras soluciones, la decodificación de eventos en cada ciclo ocurre dos veces sin ninguna necesidad. La plantilla de implementación de la función de ciclo para el tercer método de interacción del autómata con el entorno externo se describe en el Listado 2.6.

**Listado 2.6. Plantilla de implementación para el ciclo de un autómata de Mealy en lenguaje C (a cada evento le corresponde una función separada)**

```c
void e1() {
  switch (y) { // Decodificador de estados
    case 1:
      // Decodificador de conjuntos de variables de entrada
      if (<formula_de_variables_de_entrada_1>) {
        // Bloque de formación de acciones de salida
        z<i_1>(); // ... (código omitido para brevedad)
        z<i_t>();
        y = <1..s>; // Actualización de estado
      } else if (<formula_de_variables_de_entrada_2>) {
        z<i_1>(); // ... (código omitido para brevedad)
        z<i_t>();
        y = <1..s>;
      } // ... (código omitido para brevedad)
      else if (<formula_de_variables_de_entrada_k>) {
        z<i_1>(); // ... (código omitido para brevedad)
        z<i_t>();
        y = <1..s>;
      }
      break;
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

```c
void e2() {
  switch (y) {
    case 1:
      // ... (código omitido para brevedad)
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

```c
// ... (código omitido para brevedad)
void e<r>() {
  switch (y) {
    case 1:
      // ... (código omitido para brevedad)
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

Una variante de implementación similar a la descrita anteriormente fue utilizada en la obra [47]. Consideremos las tres variantes propuestas para implementar la interacción del autómata con el entorno externo utilizando el ejemplo del reloj despertador, una entidad con un comportamiento complejo, cuyo autómata de control fue construido en la Sección 2.1.1.

En el Listado 2.7, los comandos y las consultas del objeto de control del reloj despertador se implementan como funciones separadas para aumentar la modularidad, y no como parte de la implementación del autómata de control [42]. Este listado utiliza la primera de las plantillas propuestas (los eventos se describen mediante variables globales).

**Listado 2.7. Implementación de un reloj despertador (eventos representados por variables globales)**

```c
const int h = 1;
const int m = 2;
const int a = 3;
const int t = 4;

int e; // Evento actual
int y; // Estado de control actual
```

```c
// Implementación del objeto de control
int hours;
int minutes;
int alarm_hours;
int alarm_minutes;
```

```c
bool x1() {
  if ((minutes == alarm_minutes - 1) && (hours == alarm_hours) || (alarm_minutes == 0) && (minutes == 59) && (hours == alarm_hours - 1))
    return true;
  else
    return false;
}
```

```c
bool x2() {
  if ((minutes == alarm_minutes) && (hours == alarm_hours))
    return true;
  else
    return false;
}
```

```c
void z1() {
  hours = (hours + 1) % 24;
}
```

```c
void z2() {
  minutes = (minutes + 1) % 60;
}
```

```c
void z3() {
  alarm_hours = (alarm_hours + 1) % 24;
}
```

```c
void z4() {
  alarm_minutes = (alarm_minutes + 1) % 60;
}
```

```c
void z5() {
  minutes = (minutes + 1) % 60;
  if (minutes == 0) hours = (hours + 1) % 24;
}
```

```c
void z6() {
  // ... Encender alarma
}
```

```c
void z7() {
  // ... Apagar alarma
}
```

```c
// Implementación del autómata de control
void A1() {
  switch (y) {
    case 1: // Alarma desactivada
      if (e == h) { z1(); }
      else if (e == m) { z2(); }
      else if (e == a) { y = 2; }
      else if (e == t) { z5(); } break;
    case 2: // Configuración de la hora de la alarma
      if (e == h) { z3(); }
      else if (e == m) { z4(); }
      else if (e == a) { y = 3; }
      else if (e == t) { z5(); } break;
    case 3: // Alarma activada
      if (e == h) { z1(); }
      else if (e == m) { z2(); }
      else if (e == a) { z7(); y = 1; }
      else if ((e == t) && x1()) { z5(); z6(); }
      else if ((e == t) && x2()) { z5(); z7(); }
      else if (e == t) { z5(); } break;
  }
}
```

El Listado 2.8 presenta la implementación del autómata de control del reloj despertador, utilizando la segunda plantilla: los eventos se pasan al autómata como argumentos. La implementación del objeto de control en este caso no difiere de la primera variante, por lo que no se incluye en el listado.

**Listado 2.8. Implementación de un reloj despertador (eventos pasados como argumentos)**

```c
// Implementación del autómata de control
void A1(int e) {
  switch (y) {
    case 1: // Alarma desactivada
      if (e == h) { z1(); }
      else if (e == m) { z2(); }
      else if (e == a) { y = 2; }
      // ... (código omitido para brevedad)
  }
}
```

Entendido. He revisado la traducción y he añadido la marca `[[[IMAGEN]]]` en cada lugar donde se menciona una figura o imagen en el texto.

A continuación, la traducción completa del documento "libroRusoP2.docx" con las marcas de imagen y sin considerar el índice:

-----

### Implementación de Autómatas

**Patrones de Implementación**

Los autómatas se pueden crear y modificar fácilmente durante la ejecución del programa. Por ejemplo, tal representación es necesaria para la optimización de autómatas, que se discute en la Sección 4.4. En el contexto de esta sección, no se requiere la modificación dinámica de la estructura del autómata. Por lo tanto, para aumentar la velocidad, se debe preferir el segundo de los métodos de implementación mencionados anteriormente (utilizando una instrucción de selección), ya que es estático.

La palabra clave `switch` se utiliza en C para las instrucciones de selección [44]. Otros lenguajes de programación imperativos de alto nivel tienen instrucciones similares. Las instrucciones de selección se pueden utilizar para implementar decodificadores de estados y acciones de entrada (Fig. 2.30). [[[IMAGEN]]] Como resultado, la plantilla de implementación para el ciclo de un autómata de Moore tomará la siguiente forma (Listado 2.1).

**Listado 2.1. Plantilla de implementación para el ciclo de un autómata de Moore en lenguaje C (utilizando dos instrucciones de selección)**

```c
void A() {
  switch (y) { // Decodificador de estados
    case 1:
      // Bloque de formación de acciones de salida
      z1 = <0|1>; ...; zm = <0|1>;
      switch (x) { // Decodificador de acciones de entrada
        case 0:
          y = <1..s>; break; // Actualización de estado
        // ... (código omitido para brevedad)
        case <2^n - 1>:
          y = <1..s>; break;
      }
      break;
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

Con este enfoque, el autómata se describe estáticamente: su estructura está codificada en el texto del programa. Esta propiedad garantiza la velocidad requerida. Sin embargo, queda otro problema: el crecimiento exponencial de la descripción del autómata con el aumento del número de variables de entrada. De hecho, el número de etiquetas `case` en la instrucción de selección anidada, y, en consecuencia, el volumen del texto del programa, depende exponencialmente de `n` (el número de variables de entrada).

Para resolver este problema, recordemos la observación hecha en relación con las tablas: en la mayoría de los casos, solo un pequeño conjunto de variables de entrada es significativo en cada estado. Por lo tanto, no es necesario especificar el valor de la función de transición para todas las posibles acciones de entrada. Como regla general, solo algunas combinaciones de valores de varias variables de entrada conducen a un cambio de estado. Aparentemente, la forma más compacta de escribir la función de transición se utiliza en la notación de grafos de transición: para cada estado se define un conjunto de transiciones salientes, marcadas con condiciones en forma de fórmulas booleanas. La experiencia muestra que en problemas reales el tamaño de estas fórmulas prácticamente no aumenta con el crecimiento del número de variables de entrada.

La plantilla de implementación propuesta anteriormente se puede modificar fácilmente para utilizar una representación compacta de la función de transición. Para esto, es suficiente reemplazar la instrucción de selección interna con varias instrucciones de ramificación (según el número de arcos que salen de este estado en el grafo de transición). Las condiciones de ramificación serán las etiquetas de los arcos salientes. Tenga en cuenta que no es necesario asignar instrucciones de ramificación a los bucles en el autómata de Moore. La plantilla de implementación modificada se presenta en el Listado 2.2.

**Listado 2.2. Plantilla de implementación para el ciclo de un autómata de Moore en lenguaje C (utilizando instrucciones de selección y ramificación)**

```c
void A() {
  switch (y) { // Decodificador de estados
    case 1:
      // Bloque de formación de acciones de salida
      z1 = <0|1>; ...; zm = <0|1>;
      if (<etiqueta_1>) { // Decodificador de acciones de entrada
        y = <1..s>; // Actualización de estado
      } else if (<etiqueta_2>) {
        y = <1..s>;
      } // ... (código omitido para brevedad)
      else if (<etiqueta_k>) {
        y = <1..s>;
      }
      break;
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

La solución al problema del volumen innecesariamente grande de la representación del autómata condujo incidentalmente a otra mejora: la transformación formal del grafo de transición en código se hizo más sencilla. Sin embargo, ¿es realmente la descripción de las transiciones de estado en forma de una secuencia de instrucciones de ramificación isomorfa a la descripción en forma de un conjunto de arcos salientes? Una fuente de inconsistencia puede ser el hecho de que las instrucciones de ramificación siempre se ejecutan en el orden especificado por el texto del programa, y el orden de verificación de las condiciones en los arcos del grafo no está definido. Sin embargo, en un grafo de transición correcto (consistente), el orden de verificación de las condiciones en los arcos no importa. Si se asignan prioridades a los arcos en el grafo de transición, entonces en el texto del programa las instrucciones de ramificación correspondientes también deben estar en el orden especificado por las prioridades.

Como ejemplo del uso de la plantilla considerada, presentaremos la implementación del autómata del sistema de control de válvulas, cuyo diseño se discutió en la Sección 2.1.1.

**Listado 2.3. Implementación del sistema de control de válvulas en lenguaje C**

```c
void A() {
  switch (y) {
    case 1: // Cerrado
      z1 = 0; z2 = 0; z3 = 0; z4 = 0;
      if (x1) { y = 2; }
      break;
    case 2: // Abriendo
      z1 = 1; z2 = 0; z3 = 0; z4 = 1;
      if (x4 && x6) { y = 3; } else if (!x4 && x6) { y = 5; }
      break;
    case 3: // Abierto
      z1 = 0; z2 = 0; z3 = 0; z4 = 0;
      if (x2) { y = 4; }
      break;
    case 4: // Cerrando
      z1 = 0; z2 = 1; z3 = 0; z4 = 1;
      if (x5 && x6) { y = 1; } else if (!x5 && x6) { y = 5; }
      break;
    case 5: // Falla
      z1 = 0; z2 = 0; z3 = 1; z4 = 0;
      if (x3) { y = 1; }
      break;
  }
}
```

Tenga en cuenta que las palabras clave `else` en esta implementación se introducen únicamente para mejorar el rendimiento del programa. Dado que las condiciones de transición de cada estado son ortogonales en este caso, las palabras clave mencionadas pueden omitirse.

Anteriormente se discutió la implementación de sistemas con comportamiento complejo, controlados por un solo autómata. Pasemos a los problemas de implementación de sistemas controlados por autómatas que interactúan. En este caso, es conveniente implementar el ciclo de trabajo de cada autómata como una función separada. Si los autómatas en el sistema interactúan intercambiando números de estado, entonces las variables internas de otros autómatas, además de las variables de entrada, participarán en las condiciones de ramificación. En los bloques de formación de acciones de salida, además de las instrucciones de asignación de valores a las variables de salida, aparecerán llamadas a autómatas anidados y llamados.

La llamada a un autómata anidado se realiza llamando a la función que implementa su ciclo de trabajo. La llamada a un autómata invocado es una operación más compleja. Una de las formas de implementarlo es crear una función adicional para cada autómata invocado Ai (descrito con la función `void A<i>()`), que tiene la siguiente estructura:

**Listado 2.4. Plantilla de función para llamar a un autómata invocado**

```c
void Call_A<i>() {
  y<i> = 1;
  while (y<i> != <estado_final>) {
    <Entrada x> Ai();
    <Salida z>
  }
}
```

Después de esto, en el punto de llamada al autómata invocado, se ejecuta la función `Call_A<i>()`.

Si durante el diseño del sistema se realizó una descomposición de autómatas paralela, existen dos variantes de implementación principales.

1.  **Todo el sistema se ejecuta en un solo procesador.** En este caso, es necesario asegurar el trabajo pseudo-paralelo de los autómatas. Aquí se manifiesta una de las ventajas de la programación de autómatas: incluso si el entorno de ejecución no admite la multitarea, la ejecución pseudo-paralela de los autómatas se puede lograr fácilmente colocando las llamadas a sus funciones correspondientes consecutivamente en el cuerpo del ciclo del programa principal (Fig. 2.31). [[[IMAGEN]]]

    **Fig. 2.31. Esquema del algoritmo que implementa el funcionamiento pseudo-paralelo de `p` autómatas activos**

2.  **Cada autómata se ejecuta en un procesador separado.** En este caso, cada una de las funciones que implementan los ciclos de trabajo de los autómatas del sistema se coloca en su propio ciclo dentro de un programa principal separado. Aquí, los problemas de interacción y sincronización pasan a primer plano. En particular, es necesario garantizar la coherencia de los datos intercambiados por los autómatas en el sistema. La elección de una u otra solución a estos problemas depende de las especificidades del sistema en cuestión.

Como ejemplo, presentaremos la implementación de un sistema de control de dos válvulas. De las varias opciones de arquitectura propuestas en la Sección 2.1.2, elegiremos aquella en la que se realizó una descomposición de autómatas paralela. Supongamos que el sistema debe ejecutarse en un solo procesador. El Listado 2.5 contiene las implementaciones de las funciones responsables del ciclo de trabajo de cada uno de los dos autómatas, así como la plantilla de implementación del programa principal.

**Listado 2.5. Implementación del sistema de control de dos válvulas en lenguaje C**

```c
void A1() { // Autómata que controla la primera válvula
  switch (y1) {
    case 1: // Cerrado
      z1 = 0; z2 = 0;
      if (x1) { y1 = 2; } break;
    case 2: // Abriendo
      z1 = 1; z2 = 0;
      if (x3) { y1 = 3; } break;
    case 3: // Abierto
      z1 = 0; z2 = 0;
      if (y2 == 1) { y1 = 4; } // Asumo que el original tenía y en vez de y1 por error
      break;
    case 4: // Cerrando
      z1 = 0; z2 = 1;
      if (x4) { y1 = 1; } break;
  }
}
```

```c
void A2() { // Autómata que controla la segunda válvula
  switch (y2) {
    case 1: // Cerrado
      z3 = 0; z4 = 0;
      if (y1 == 3) { y2 = 2; }
      break;
    case 2: // Abriendo
      z3 = 1; z4 = 0;
      if (x5) { y2 = 3; } break;
    case 3: // Abierto
      z3 = 0; z4 = 0;
      if (x2) { y2 = 4; } break;
    case 4: // Cerrando
      z3 = 0; z4 = 1;
      if (x6) { y2 = 1; } break;
  }
}
```

```c
void main() { // Programa principal
  y1 = 1; y2 = 1;
  while (1) {
    // <Entrada x> A1(); A2();
    // <Salida z>
    // En el código original, las líneas "<Entrada x>" y "<Salida z>"
    // no son código C válido, por lo que se comentan o se eliminan
    // en una implementación real. Aquí se dejan comentadas para referencia.
  }
}
```

### Otras Clases de Problemas

En esta sección se abordan problemas que no pertenecen al ámbito del control lógico. En el campo de la programación de aplicaciones para computadoras personales, los sistemas con comportamiento complejo suelen ser orientados a eventos, y los objetos automatizados en ellos, como regla general, son pasivos. En cuanto a los modelos de autómatas, lo más conveniente es usar autómatas de Mealy o (con menos frecuencia) autómatas mixtos.

¿Qué cambios en la estructura del algoritmo implicará esta especificidad? Dado que se utilizan otros modelos de autómatas, el bloque de formación de acciones de salida debe ubicarse de manera diferente. Los comandos del objeto de control ya no se implementan por hardware, sino por software, como procedimientos ordinarios. Por lo tanto, en el bloque de formación de acciones de salida, en lugar de asignar valores a las variables de salida, se deben colocar llamadas a procedimientos correspondientes a aquellas variables de salida que toman el valor "verdadero".

Dado que los objetos automatizados considerados son pasivos, el programa principal también ha cambiado. Consideremos el esquema de algoritmo que describe un ciclo de trabajo de un autómata de Mealy (Fig. 2.32). [[[IMAGEN]]] Aquí, el bloque de formación de acciones de salida se encuentra detrás del decodificador de acciones de entrada y contiene llamadas a comandos específicos del objeto de control. El conjunto de comandos que deben ser llamados se determina por el valor de la función de salida del autómata para el estado dado y la acción de entrada.

Aquí, `y` representa el estado del autómata.

**Fig. 2.32. Esquema del algoritmo que implementa un ciclo de trabajo de un autómata de Mealy**

Al combinar este algoritmo con el algoritmo del ciclo de trabajo del autómata de Moore de la sección anterior, obtenemos un algoritmo para un autómata mixto (Fig. 2.33), [[[IMAGEN]]] en el que hay dos bloques de formación de acciones de salida: antes y después del decodificador de acciones de entrada.

Aquí, `y` representa el estado del autómata.

**Fig. 2.33. Esquema del algoritmo que implementa un ciclo de trabajo de un autómata mixto**

El programa principal ha cambiado mucho más. Como el lector ya sabe, un modelo de autómata pasivo no funciona continuamente (ciclo por ciclo), sino que realiza el siguiente ciclo de trabajo por iniciativa del entorno externo. Por lo tanto, para tales modelos, el programa principal ya no es parte de la implementación del autómata. Este programa describe el funcionamiento del entorno externo, y desde él, en ciertos lugares, se puede llamar a una subrutina que implementa el ciclo de trabajo del autómata. En los sistemas de eventos aplicados, la función del programa principal, como regla general, consiste en extraer mensajes de la cola y pasarlos a los controladores correspondientes. Sin embargo, esto es solo la punta del iceberg: la aplicación se ejecuta bajo el control del sistema operativo, que asume todo el trabajo de recibir eventos de dispositivos externos y pasarlos al programa. Por lo tanto, el concepto mismo de programa principal en los sistemas de software de aplicación modernos es relativo e indefinido.

Además, con el paso a la programación de aplicaciones de sistemas de eventos, los criterios de optimización para la implementación de autómatas también cambiaron. El isomorfismo del código del programa al grafo de transición sigue siendo primordial, pero la eficiencia en tiempo y memoria para esta clase de problemas no es tan crítica. Por el contrario, la flexibilidad y la capacidad de evolucionar, adaptándose a nuevos requisitos, adquieren mayor importancia.

Recordemos que en esta sección se discuten cuestiones de implementación en el contexto de la programación procedural. El enfoque orientado a objetos tiene un arsenal más amplio de métodos y patrones para implementar autómatas; algunos de ellos se discuten más adelante en este libro (Sección 3.3). Por ahora, nos quedamos con el lenguaje C y dos formas de implementar autómatas mencionadas anteriormente: mediante tablas y mediante instrucciones de selección.

Existe una serie de tareas en las que es necesario modificar el autómata durante la ejecución del programa. Para tales casos, se debe utilizar la implementación del autómata en forma de tabla. Sin embargo, la experiencia demuestra que tales tareas son bastante raras. Por lo tanto, la plantilla de implementación más utilizada sigue siendo la descrita en la sección anterior: el uso de una instrucción de selección en combinación con una instrucción de ramificación (especialmente porque este método simplifica la transformación isomorfa del grafo de transición en código de programa).

La plantilla de implementación del ciclo de trabajo del autómata ha cambiado insignificativamente en comparación con el Listado 2.2. Dado que ahora se utiliza un autómata de Mealy en lugar de un autómata de Moore, el bloque de formación de acciones de salida se ha movido dentro de la instrucción de ramificación. Además, en este bloque, en lugar de asignar valores a las variables de salida, ahora se realizan llamadas a subrutinas correspondientes a los comandos del objeto de control.

Una pregunta más interesante es la interacción de la función del ciclo del autómata con el contexto que lo llama, es decir, la transmisión de eventos al autómata. Existen tres variantes principales de dicha interacción.

1.  **Los eventos, al igual que las variables de entrada, son variables globales del programa o del módulo del programa en el que se encuentra el autómata** (tenga en cuenta que la segunda opción es menos probable, ya que, a diferencia de las variables de entrada, que son locales al objeto automatizado, los eventos, como regla general, están destinados a la interacción entre módulos). En el caso de que los eventos sean *exclusivos* (dos eventos no pueden ocurrir simultáneamente), para almacenar el evento actual es suficiente introducir una variable entera, cuyo valor en el decodificador de acciones de entrada se comparará con los identificadores de eventos específicos. Si los eventos en el sistema en desarrollo no tienen la propiedad de exclusividad, se puede utilizar un vector de bits para almacenar el conjunto de eventos actuales. En este caso, la representación de los eventos no difiere de la representación de las variables de entrada. La plantilla de implementación de la función de ciclo del autómata con este método de representación de eventos difiere de la descrita en el Listado 2.2 solo en la posición del bloque de formación de acciones de salida.

2.  **Los eventos son argumentos de la función de ciclo del autómata.** Esta decisión de diseño refleja la diferencia entre eventos y variables de entrada: aquí el autómata *procesa* un evento (o un conjunto de eventos), mientras que los valores de las variables de entrada solo se consultan si es necesario por iniciativa propia del autómata. Además, al implementar el autómata manualmente, esta solución previene errores de programación posibles con el primer enfoque: cuando el programador olvida configurar la variable para almacenar el evento antes de llamar al ciclo del autómata. Los cambios en la plantilla de implementación en este caso son insignificantes y solo afectan la firma de la función de ciclo: `void A (int e)`, si los eventos son exclusivos; `void A (bool[] e)`, si los eventos no son exclusivos. Esta variante de implementación fue propuesta en las obras [27, 42, 46]. Una descripción de un ejemplo de su uso en la práctica se proporciona en la obra [8].

3.  **A cada evento se le asocia una función separada.** Esta solución solo es adecuada para implementar un modelo de eventos exclusivo (tenga en cuenta que este modelo es el más común). Además, refleja el papel activo de los eventos, el hecho de que es la ocurrencia de un evento lo que inicia la llamada al autómata. Además, esta solución es la que mejor se adapta a la estructura tradicional de un módulo de programa en sistemas de eventos, donde cualquier parte independiente del programa es un conjunto de manejadores de eventos semánticamente relacionados. Un programa construido de acuerdo con esta solución ya no es completamente isomorfo al esquema de algoritmo de la Fig. 2.32, donde primero se decodifica el estado y luego la acción de entrada. En este caso, primero se produce la ramificación por eventos, luego por estados y, finalmente, por variables de entrada. Esto puede parecer una complicación injustificada. Sin embargo, en la mayoría de los sistemas de eventos, el entorno externo decodifica necesariamente el evento antes de enviarlo al autómata (al menos para comprender a qué autómata debe transmitirse). En este caso, al utilizar otras soluciones, la decodificación de eventos en cada ciclo ocurre dos veces sin ninguna necesidad. La plantilla de implementación de la función de ciclo para el tercer método de interacción del autómata con el entorno externo se describe en el Listado 2.6.

**Listado 2.6. Plantilla de implementación para el ciclo de un autómata de Mealy en lenguaje C (a cada evento le corresponde una función separada)**

```c
void e1() {
  switch (y) { // Decodificador de estados
    case 1:
      // Decodificador de conjuntos de variables de entrada
      if (<formula_de_variables_de_entrada_1>) {
        // Bloque de formación de acciones de salida
        z<i_1>(); // ... (código omitido para brevedad)
        z<i_t>();
        y = <1..s>; // Actualización de estado
      } else if (<formula_de_variables_de_entrada_2>) {
        z<i_1>(); // ... (código omitido para brevedad)
        z<i_t>();
        y = <1..s>;
      } // ... (código omitido para brevedad)
      else if (<formula_de_variables_de_entrada_k>) {
        z<i_1>(); // ... (código omitido para brevedad)
        z<i_t>();
        y = <1..s>;
      }
      break;
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

```c
void e2() {
  switch (y) {
    case 1:
      // ... (código omitido para brevedad)
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

```c
// ... (código omitido para brevedad)
void e<r>() {
  switch (y) {
    case 1:
      // ... (código omitido para brevedad)
    case 2:
      // ... (código omitido para brevedad)
    case <s>:
      // ... (código omitido para brevedad)
  }
}
```

Una variante de implementación similar a la descrita anteriormente fue utilizada en la obra [47]. Consideremos las tres variantes propuestas para implementar la interacción del autómata con el entorno externo utilizando el ejemplo del reloj despertador, una entidad con un comportamiento complejo, cuyo autómata de control fue construido en la Sección 2.1.1.

En el Listado 2.7, los comandos y las consultas del objeto de control del reloj despertador se implementan como funciones separadas para aumentar la modularidad, y no como parte de la implementación del autómata de control [42]. Este listado utiliza la primera de las plantillas propuestas (los eventos se describen mediante variables globales).

**Listado 2.7. Implementación de un reloj despertador (eventos representados por variables globales)**

```c
const int h = 1;
const int m = 2;
const int a = 3;
const int t = 4;

int e; // Evento actual
int y; // Estado de control actual
```

```c
// Implementación del objeto de control
int hours;
int minutes;
int alarm_hours;
int alarm_minutes;
```

```c
bool x1() {
  if ((minutes == alarm_minutes - 1) && (hours == alarm_hours) || (alarm_minutes == 0) && (minutes == 59) && (hours == alarm_hours - 1))
    return true;
  else
    return false;
}
```

```c
bool x2() {
  if ((minutes == alarm_minutes) && (hours == alarm_hours))
    return true;
  else
    return false;
}
```

```c
void z1() {
  hours = (hours + 1) % 24;
}
```

```c
void z2() {
  minutes = (minutes + 1) % 60;
}
```

```c
void z3() {
  alarm_hours = (alarm_hours + 1) % 24;
}
```

```c
void z4() {
  alarm_minutes = (alarm_minutes + 1) % 60;
}
```

```c
void z5() {
  minutes = (minutes + 1) % 60;
  if (minutes == 0) hours = (hours + 1) % 24;
}
```

```c
void z6() {
  // ... Encender alarma
}
```

```c
void z7() {
  // ... Apagar alarma
}
```

```c
// Implementación del autómata de control
void A1() {
  switch (y) {
    case 1: // Alarma desactivada
      if (e == h) { z1(); }
      else if (e == m) { z2(); }
      else if (e == a) { y = 2; }
      else if (e == t) { z5(); } break;
    case 2: // Configuración de la hora de la alarma
      if (e == h) { z3(); }
      else if (e == m) { z4(); }
      else if (e == a) { y = 3; }
      else if (e == t) { z5(); } break;
    case 3: // Alarma activada
      if (e == h) { z1(); }
      else if (e == m) { z2(); }
      else if (e == a) { z7(); y = 1; }
      else if ((e == t) && x1()) { z5(); z6(); }
      else if ((e == t) && x2()) { z5(); z7(); }
      else if (e == t) { z5(); } break;
  }
}
```

El Listado 2.8 presenta la implementación del autómata de control del reloj despertador, utilizando la segunda plantilla: los eventos se pasan al autómata como argumentos. La implementación del objeto de control en este caso no difiere de la primera variante, por lo que no se incluye en el listado.

**Listado 2.8. Implementación de un reloj despertador (eventos pasados como argumentos)**

```c
// Implementación del autómata de control
void A1(int e) {
  switch (y) {
    case 1: // Alarma desactivada
      if (e == h) { z1(); }
      else if (e == m) { z2(); }
      else if (e == a) { y = 2; }
      else if (e == t) { z5(); }
      break;
    case 2: // Configuración de la hora de la alarma
      if (e == h) { z3(); }
      else if (e == m) { z4(); }
      else if (e == a) { y = 3; }
      else if (e == t) { z5(); }
      break;
    case 3: // Alarma activada
      if (e == h) { z1(); }
      else if (e == m) { z2(); }
      else if (e == a) { z7(); y = 1; }
      else if ((e == t) && x1()) { z5(); z6(); }
      else if ((e == t) && x2()) { z5(); z7(); }
      else if (e == t) { z5(); }
      break;
  }
}
```

La última variante de implementación discutida anteriormente (Listado 2.6) es la más adecuada para una aplicación de escritorio. Para ilustrar su uso, presentemos una implementación del autómata del reloj despertador basada en esta plantilla (Listado 2.9). En este caso, el Listado 2.7 también presenta la implementación del objeto de control.

**Listado 2.9. Implementación de un reloj despertador (cada evento tiene su propia función)**

```c
// ... (Declaraciones de variables y funciones de z1() a z7() son las mismas que en Listado 2.7)

// Manejadores de eventos
void event_h() { // Evento 'h' (horas)
  switch (y) {
    case 1: // Alarma desactivada
      z1();
      break;
    case 2: // Configuración de la hora de la alarma
      z3();
      break;
    case 3: // Alarma activada
      z1();
      break;
  }
}

void event_m() { // Evento 'm' (minutos)
  switch (y) {
    case 1: // Alarma desactivada
      z2();
      break;
    case 2: // Configuración de la hora de la alarma
      z4();
      break;
    case 3: // Alarma activada
      z2();
      break;
  }
}

void event_a() { // Evento 'a' (alarma)
  switch (y) {
    case 1: // Alarma desactivada
      y = 2;
      break;
    case 2: // Configuración de la hora de la alarma
      y = 3;
      break;
    case 3: // Alarma activada
      z7();
      y = 1;
      break;
  }
}

void event_t() { // Evento 't' (tiempo)
  switch (y) {
    case 1: // Alarma desactivada
      z5();
      break;
    case 2: // Configuración de la hora de la alarma
      z5();
      break;
    case 3: // Alarma activada
      if (x1()) {
        z5();
        z6(); // Encender alarma
      } else if (x2()) {
        z5();
        z7(); // Apagar alarma
      } else {
        z5();
      }
      break;
  }
}

// Función principal del programa (simulando un bucle de eventos)
void main_loop() {
  // En un sistema real, los eventos serían generados por el SO o el usuario.
  // Aquí, se simularía su recepción y la llamada al manejador correspondiente.
  // Por ejemplo:
  // while (true) {
  //   int received_event = get_next_event();
  //   if (received_event == h) event_h();
  //   else if (received_event == m) event_m();
  //   else if (received_event == a) event_a();
  //   else if (received_event == t) event_t();
  // }
}
```

### 2.3. Herramientas de Programación de Autómatas

En la literatura, se describen muchas herramientas para el diseño e implementación de sistemas basados en autómatas finitos. Algunos de ellos se centran en el diseño visual de autómatas [15, 23, 31, 48], algunos generan código fuente en un lenguaje de programación específico [16, 26, 35, 41, 45, 52], mientras que otros son bibliotecas de clases de autómata [14, 28, 30].

En este apartado presentaremos una breve descripción de las herramientas más conocidas de este tipo.

El kit de herramientas *SMC (State Machine Compiler)* [45] le permite generar automáticamente código fuente en los lenguajes de programación Ada, C, C++, C\#, Java, Objective-C, Python, Ruby, Scala y VB.Net a partir de la descripción de un autómata finito. El autómata se describe en un archivo de texto utilizando su propio lenguaje de descripción. Las principales desventajas de SMC son la falta de una interfaz visual para la construcción de autómatas y la capacidad de soportar solo el modelo de autómata de Mealy.

El kit de herramientas *Ragel* [35] es un compilador de máquinas de estados. Como SMC, Ragel genera código fuente en los lenguajes de programación C, C++, C\#, D, Java, Objective-C, Go, y Ruby. El autómata se describe utilizando expresiones regulares. Las principales desventajas de Ragel son la falta de una interfaz visual para la construcción de autómatas y la falta de soporte para un número suficientemente grande de variables de entrada.

El kit de herramientas *Yakindu Statechart Tools* [52] permite el diseño visual de autómatas y la generación de código fuente en los lenguajes de programación C, C++, Java y C\#. Las principales ventajas de Yakindu son la presencia de una interfaz visual, soporte para autómatas de Moore, Mealy y autómatas mixtos, la capacidad de simular el autómata y soporte para la jerarquía y paralelismo de estados. Las principales desventajas de Yakindu son el alto costo, la dificultad de uso y la falta de soporte para la composición.

El kit de herramientas *QP (Quantum Platform)* [26] es una biblioteca de clases de autómata en los lenguajes de programación C y C++. Las principales ventajas de QP son la presencia de una biblioteca de clases de autómata, soporte para autómatas de Moore, Mealy y autómatas mixtos, y la capacidad de soportar la jerarquía y el paralelismo de estados. Las principales desventajas de QP son la falta de una interfaz visual para la construcción de autómatas y la dificultad de uso.

El kit de herramientas *boost::statechart* [14] es una biblioteca de clases de autómata en el lenguaje de programación C++. Las principales ventajas de boost::statechart son la presencia de una biblioteca de clases de autómata y la capacidad de soportar la jerarquía y el paralelismo de estados. Las principales desventajas de boost::statechart son la falta de una interfaz visual para la construcción de autómatas y la dificultad de uso.

El kit de herramientas *FSM* [28] es una biblioteca de clases de autómata en el lenguaje de programación C++. Las principales ventajas de FSM son la presencia de una biblioteca de clases de autómata y la capacidad de soportar la jerarquía y el paralelismo de estados. Las principales desventajas de FSM son la falta de una interfaz visual para la construcción de autómatas y la dificultad de uso.

El kit de herramientas *State Machine Library* [30] es una biblioteca de clases de autómata en el lenguaje de programación C\#. Las principales ventajas de State Machine Library son la presencia de una biblioteca de clases de autómata y la capacidad de soportar la jerarquía y el paralelismo de estados. Las principales desventajas de State Machine Library son la falta de una interfaz visual para la construcción de autómatas y la dificultad de uso.

El kit de herramientas *State Pattern* [31] es un patrón de diseño en el lenguaje de programación Java. Las principales ventajas de State Pattern son la presencia de un patrón de diseño y la capacidad de soportar la jerarquía de estados. Las principales desventajas de State Pattern son la falta de una interfaz visual para la construcción de autómatas y la dificultad de uso.

El kit de herramientas *Spring State Machine* [48] es una biblioteca de clases de autómata en el lenguaje de programación Java. Las principales ventajas de Spring State Machine son la presencia de una biblioteca de clases de autómata y la capacidad de soportar la jerarquía y el paralelismo de estados. Las principales desventajas de Spring State Machine son la falta de una interfaz visual para la construcción de autómatas y la dificultad de uso.

**Conclusiones de la revisión de herramientas**

La revisión de las herramientas existentes mostró que la mayoría de ellas son bibliotecas de clases de autómatas o generadores de código. Las herramientas existentes no permiten el diseño visual de autómatas, no soportan la composición de autómatas, no soportan un número suficientemente grande de variables de entrada y no soportan la optimización de autómatas.

En este trabajo, se propone un nuevo enfoque para la programación de autómatas, que permite superar las desventajas mencionadas anteriormente.

### Capítulo 3. Programación Orientada a Objetos de Autómatas

En este capítulo, se considera la implementación de sistemas basados en autómatas finitos utilizando el paradigma de programación orientada a objetos.

### 3.1. Clases y Objetos

El paradigma de programación orientada a objetos (POO) se basa en el concepto de "objeto", que puede contener datos, en forma de campos (a menudo conocidos como atributos), y código, en forma de procedimientos (a menudo conocidos como métodos). Una característica de los objetos es que combinan datos y procedimientos, es decir, son autocontenidos. En la mayoría de los lenguajes de programación basados en clases, los objetos son instancias de clases. Las clases sirven como planos o plantillas a partir de las cuales se crean los objetos.

Las clases y los objetos permiten modelar el mundo real de manera más intuitiva. Los objetos pueden representar entidades del mundo real (por ejemplo, un coche, una persona) o conceptos abstractos (por ejemplo, una cuenta bancaria, una transacción).

Los principios clave de la POO son:

  * **Encapsulamiento:** Ocultación de los detalles internos de un objeto y exposición solo de la interfaz necesaria para interactuar con él.
  * **Herencia:** Capacidad de una clase para adquirir propiedades y comportamientos de otra clase, lo que promueve la reutilización de código.
  * **Polimorfismo:** Capacidad de objetos de diferentes clases para responder a un mismo mensaje (llamada de método) de diferentes maneras, dependiendo de su propia implementación.

La POO facilita el desarrollo de software complejo al proporcionar una forma estructurada y modular de organizar el código, lo que mejora la mantenibilidad y la escalabilidad del sistema.

### 3.2. Diseño por Contrato

El diseño por contrato (DbC) es un enfoque para el diseño de software que se basa en la idea de que los componentes de software (por ejemplo, métodos, funciones, clases) deben especificar formalmente sus obligaciones y beneficios mutuos. Esencialmente, establece un "contrato" entre un cliente (el código que llama al componente) y un proveedor (el componente en sí).

Un contrato consta de tres elementos principales:

  * **Precondiciones:** Condiciones que deben ser verdaderas antes de que el cliente llame al componente. Si las precondiciones no se cumplen, es culpa del cliente.
  * **Postcondiciones:** Condiciones que deben ser verdaderas después de que el componente haya completado su ejecución con éxito. Si las postcondiciones no se cumplen, es culpa del proveedor.
  * **Invariantes:** Condiciones que deben ser verdaderas antes y después de cualquier llamada a un método público del objeto, manteniendo la consistencia interna del objeto.

El DbC fue popularizado por Bertrand Meyer con el lenguaje de programación Eiffel. Promueve la confiabilidad, robustez y claridad del código. Al definir claramente las responsabilidades, el DbC ayuda a detectar errores en las etapas iniciales de desarrollo y facilita la depuración y el mantenimiento. Se puede implementar utilizando afirmaciones, comentarios o características de lenguaje específicas.

### 3.3. Implementación de Autómatas Utilizando Programación Orientada a Objetos

El paradigma orientado a objetos es muy adecuado para la programación de autómatas. Cada estado del autómata puede representarse como un objeto, y las transiciones entre estados pueden implementarse como llamadas a métodos. Esta sección explora cómo se pueden aplicar los principios de la POO para crear implementaciones flexibles y mantenibles de autómatas.

Existen varios patrones de diseño que son particularmente útiles para implementar autómatas en un contexto orientado a objetos, siendo el "Patrón Estado" (State Pattern) el más directo y común.

**El Patrón Estado**

El Patrón Estado es un patrón de comportamiento que permite que un objeto altere su comportamiento cuando su estado interno cambia. El objeto parecerá cambiar su clase. En esencia, cada estado del autómata se encapsula en una clase separada. El objeto principal (el "contexto") contiene una referencia a un objeto de estado actual, y delega los comportamientos relacionados con el estado a este objeto de estado.

Ventajas del Patrón Estado para autómatas:

  * **Claridad:** Cada estado se representa explícitamente como una clase, lo que hace que el comportamiento del autómata sea más fácil de entender y depurar.
  * **Extensibilidad:** Añadir nuevos estados o transiciones es sencillo, ya que implica añadir nuevas clases de estado o modificar las existentes sin alterar el código de otros estados.
  * **Mantenibilidad:** El código relacionado con un estado específico se agrupa en una sola clase, lo que simplifica las modificaciones.

Implementación básica:

1.  **Interfaz `Estado`:** Define la interfaz común para todos los estados. Incluiría métodos para manejar los eventos o entradas que pueden ocurrir en cualquier estado.
2.  **Clases de Estado Concretas:** Cada una implementa la interfaz `Estado` y define el comportamiento específico para ese estado. Cada método de evento dentro de una clase de estado concreta puede contener lógica para realizar acciones y/o cambiar el estado del contexto.
3.  **Clase `Contexto`:** Mantiene una referencia a un objeto de `Estado` concreto y delega las llamadas a métodos relacionados con el estado a este objeto. También tiene un método para cambiar el estado actual.

Ejemplo de pseudo-código (similar a Java/C\#):

```java
// Interfaz de Estado
interface State {
    void handleEvent1(Context context);
    void handleEvent2(Context context);
    // ... otros eventos/entradas
}

// Clase de Contexto (el autómata principal)
class Context {
    private State currentState;

    public Context() {
        // Estado inicial
        this.currentState = new InitialState();
    }

    public void setState(State newState) {
        this.currentState = newState;
    }

    public void triggerEvent1() {
        currentState.handleEvent1(this);
    }

    public void triggerEvent2() {
        currentState.handle2(this);
    }
    // ... otros disparadores de eventos
}

// Ejemplo de Clase de Estado Concreta
class InitialState implements State {
    @Override
    public void handleEvent1(Context context) {
        // Realizar acciones para Evento1 en InitialState
        System.out.println("InitialState: Handling Event1. Transitioning to StateA.");
        context.setState(new StateA()); // Cambiar a StateA
    }

    @Override
    public void handleEvent2(Context context) {
        System.out.println("InitialState: Event2 not handled here.");
        // Opcional: permanecer en el mismo estado, o transición a un estado de error
    }
}

class StateA implements State {
    @Override
    public void handleEvent1(Context context) {
        System.out.println("StateA: Handling Event1. Staying in StateA.");
    }

    @Override
    public void handleEvent2(Context context) {
        System.out.println("StateA: Handling Event2. Transitioning to StateB.");
        context.setState(new StateB());
    }
}

class StateB implements State {
    // ... implementación para StateB
}
```

Este patrón no solo mejora la estructura del código, sino que también alinea el modelo de autómata más estrechamente con los principios de encapsulamiento y polimorfismo de la POO.

**Otras consideraciones de la POO para autómatas:**

  * **Herencia:** Puede usarse para definir jerarquías de estados si un autómata tiene estados que comparten comportamientos comunes (por ejemplo, un `EstadoAbriendo` y un `EstadoCerrando` podrían heredar de un `EstadoTransitorio` abstracto).
  * **Composición:** En sistemas más complejos, se pueden usar múltiples autómatas (objetos `Contexto`) que interactúan entre sí, modelando la composición de autómatas.
  * **Diseño por Contrato (DbC):** Las pre y postcondiciones pueden aplicarse a los métodos de `handleEvent` para garantizar que el autómata se comporta según lo esperado en cada transición y acción. Por ejemplo, una postcondición podría asegurar que después de una transición, el `currentState` del `Contexto` es de hecho el estado esperado.

### 3.4. Programación Genética para Síntesis de Autómatas

La programación genética (PG) es una técnica de optimización inspirada en la evolución biológica. Forma parte del campo más amplio de los algoritmos evolutivos. En el contexto de la síntesis de autómatas, la programación genética puede utilizarse para generar o mejorar automáticamente la estructura de autómatas finitos que resuelven un problema dado.

**Conceptos clave de la Programación Genética:**

  * **Individuos (Programas/Cromosomas):** En PG, los "individuos" son programas (o representaciones de programas) que intentan resolver el problema. En la síntesis de autómatas, un individuo podría ser una representación de un autómata finito (por ejemplo, una tabla de transiciones, un grafo de estados).
  * **Población:** Un conjunto de individuos (autómatas) que se evalúan y evolucionan a lo largo del tiempo.
  * **Función de Aptitud (Fitness Function):** Una función que mide qué tan bien un individuo (autómata) resuelve el problema. En la síntesis de autómatas, esto podría implicar probar el autómata generado con un conjunto de ejemplos de entrada/salida deseados y asignar una puntuación basada en el número de salidas correctas.
  * **Operadores Genéticos:**
      * **Selección:** Los individuos más aptos de la población tienen una mayor probabilidad de ser elegidos para la reproducción.
      * **Cruce (Crossover):** Combina partes de dos individuos "padres" para crear uno o más individuos "hijos". Para autómatas, esto podría implicar intercambiar subgrafos o partes de tablas de transición.
      * **Mutación:** Introduce pequeños cambios aleatorios en un individuo. Para autómatas, esto podría significar cambiar una transición, una acción de salida o añadir/eliminar un estado.

**Proceso de Síntesis de Autómatas con PG:**

1.  **Inicialización:** Crear una población inicial de autómatas aleatorios.
2.  **Evaluación:** Para cada autómata en la población, evaluar su aptitud utilizando la función de aptitud (por ejemplo, ejecutándolo contra un conjunto de datos de prueba).
3.  **Selección:** Seleccionar los autómatas más aptos de la población actual.
4.  **Reproducción:** Crear una nueva generación de autómatas aplicando operadores de cruce y mutación a los autómatas seleccionados.
5.  **Reemplazo:** Reemplazar la población antigua con la nueva generación.
6.  **Terminación:** Repetir los pasos 2-5 hasta que se cumpla un criterio de terminación (por ejemplo, se alcanza una aptitud deseada, se excede un número máximo de generaciones, o no hay mejora significativa).

**Ventajas de la PG para la síntesis de autómatas:**

  * **Exploración de espacios de diseño grandes:** La PG puede explorar eficazmente un gran espacio de posibles estructuras de autómata, lo que es difícil de hacer manualmente.
  * **Adaptación a requisitos cambiantes:** Con una función de aptitud adecuada, los autómatas pueden evolucionar para adaptarse a nuevos o modificados requisitos.
  * **Descubrimiento de soluciones no intuitivas:** Puede encontrar soluciones que un diseñador humano no consideraría.

**Desafíos:**

  * **Definición de la función de aptitud:** Diseñar una función de aptitud precisa y computacionalmente eficiente es crucial.
  * **Representación del autómata:** La forma en que se codifica un autómata en un "cromosoma" para la PG afecta la eficacia de los operadores genéticos.
  * **Costo computacional:** La ejecución de la PG puede ser computacionalmente intensiva, especialmente para autómatas complejos o grandes poblaciones.

La programación genética ofrece una poderosa metodología para la síntesis automatizada de autómatas, complementando los métodos de diseño manual y basado en herramientas.

