### Planificador de Inversión y Metas de Ahorro

Una calculadora interactiva y precisa desarrollada con **JavaScript nativo (Vanilla)** diseñada para asistir a los usuarios en la planificación financiera orientada al retiro. El sistema evalúa el estado financiero actual y traza una meta de ahorro automatizada y progresiva, adaptada milimétricamente al **mes exacto de vida** del usuario. 

La lógica central del algoritmo se rige bajo un principio de ahorro continuo: **acumular el equivalente a un año de salario íntegro por cada década transcurrida a partir de los 20 años de edad**. 

### 🚀 Características Clave

* **Cálculo de Plazos Dinámicos:** En lugar de operar con bloques redondeados de años, el motor convierte la edad del usuario a meses totales de vida para dictaminar el tiempo real de inversión remanente (120 - mesesVividos) hasta su próximo hito generacional (30, 40, 50 años, etc.).
* **Formateo de Moneda en Tiempo Real:** Interfaz enriquecida que captura y sanitiza las entradas del usuario a través de expresiones regulares (/\D/g), proyectando separadores de miles de estilo regional (de-DE) en tiempo real mientras retiene los valores numéricos puros en atributos data-valor.
* **Control Estricto de Errores y Validaciones:** Sistema blindado que neutraliza el ingreso de salarios inexistentes (<= 0), restringe el cálculo para menores de 20 años mediante un aviso de cortesía y bloquea de raíz la selección de fechas futuras en el calendario de forma nativa.

### 🛠️ Tecnologías Utilizadas

* **HTML5:** Estructuración semántica de componentes y entradas de datos.
* **CSS3:** Diseño responsivo y estilización de la interfaz de usuario (vinculado mediante styles.css).
* **JavaScript (ES6+):** Programación orientada a eventos (addEventListener), desestructuración de objetos, expresiones regulares avanzadas, lógica matemática pura (Math.floor) y formateo regionalizado de datos financieros (toLocaleString).

### 📐 Lógica Matemática Destacada

El cálculo del plazo dinámico se estructuró aislando matemáticamente el residuo de los años transcurridos en la década actual para deducir el remanente exacto de meses hacia el hito objetivo: 

javascript

const proximaEdadRedonda = (Math.floor(anios / 10) + 1) * 10;
const mesesVividos = (((anios - (Math.floor(anios / 10) * 10) ) * 12) + meses);
const tiempoRestante = 120 - mesesVividos;

Usa el código con precaución.

### 📦 Instalación y Uso

1. Clona este repositorio o descarga los archivos fuentes.
2. Asegúrate de mantener los archivos index.html y styles.css en la misma raíz del directorio.
3. Abre el archivo index.html en cualquier navegador web moderno para ejecutar la aplicación de forma local.