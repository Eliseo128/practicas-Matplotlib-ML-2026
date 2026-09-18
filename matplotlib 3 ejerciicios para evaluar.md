Aquí tienes una propuesta de 3 ejercicios prácticos contextualizados, diseñados para evaluar la comprensión lógica y el uso de Matplotlib en alumnos de tercer semestre:

### **Ejercicio 1: Análisis de Hábitos de Sueño** *(Evaluación de Gráficos de Barras)*

* **Contexto:** El departamento de orientación realizó una encuesta a 5 compañeros sobre cuántas horas duermen en promedio antes de un examen.
* **Datos a utilizar:**
* Alumnos: `['Ana', 'Luis', 'Carla', 'Diego', 'Sofía']`
* Horas de sueño: `[5, 8, 4, 6, 7]`


* **Instrucciones para el alumno:**
1. Crea el archivo `evaluacion7a-0777.py`.
2. Genera un gráfico de barras donde el eje X sean los alumnos y el eje Y las horas de sueño.
3. Aplica un color verde a las barras y agrega la cuadrícula únicamente en el eje Y.
4. Agrega una línea horizontal de referencia en el valor `7` (horas recomendadas) de color rojo y punteada.



---

### **Ejercicio 2: Rendimiento Deportivo** *(Evaluación de Gráficos de Dispersión y Relación)*

* **Contexto:** Un entrenador de fútbol quiere saber si entrenar más días a la semana ayuda a meter más goles durante el torneo escolar.
* **Datos a utilizar:**
* Días de entrenamiento a la semana: `[1, 2, 2, 3, 4, 4, 5, 5]`
* Goles anotados en el torneo: `[1, 2, 1, 4, 5, 7, 6, 9]`


* **Instrucciones para el alumno:**
1. Crea el archivo `evaluacion7b-0777.py`.
2. Grafica los datos utilizando un gráfico de dispersión (`scatter plot`).
3. Utiliza marcadores en forma de estrella (`*`) de color azul y de tamaño destacado.
4. Personaliza los títulos: Eje X ("Días de Entrenamiento"), Eje Y ("Goles Anotados") y Título Principal ("Relación Entrenamiento vs Goles").
5. **Pregunta de reflexión (en comentario dentro del código):** ¿Existe una relación positiva entre entrenar más y meter más goles?



---

### **Ejercicio 3: Presupuesto para la Fiesta de Graduación** *(Evaluación de Gráficos Circulares)*

* **Contexto:** El comité escolar está planeando los gastos para el convivio de fin de semestre y necesita presentar la distribución del presupuesto a la clase.
* **Datos a utilizar:**
* Conceptos: `['Música/DJ', 'Comida y Bebida', 'Decoración', 'Renta del Local']`
* Costos (en MXN): `[2000, 4500, 1500, 3000]`


* **Instrucciones para el alumno:**
1. Crea el archivo `evaluacion7c-0777.py`.
2. Diseña un gráfico de pastel que muestre el porcentaje correspondiente a cada concepto.
3. Aplica la propiedad para resaltar o desplegar ("explode") la rebanada correspondiente a **"Comida y Bebida"**.
4. Muestra los porcentajes con un decimal de precisión (`autopct='%1.1f%%'`) y asigna una paleta de 4 colores diferentes.



---

### **Criterios Generales de Evaluación (Rúbrica rápida)**

| Criterio | Puntuación |
| --- | --- |
| **Sintaxis y Ejecución** | El código corre sin errores en el entorno `.venv7`. *(40%)* |
| **Uso de Matplotlib** | Utiliza la función correcta (`bar`, `scatter`, `pie`) con sus etiquetas. *(30%)* |
| **Personalización Visual** | Incluye títulos, colores personalizados y etiquetas en ejes. *(20%)* |
| **Estructura de Archivos** | Nombrado correcto de los archivos de entrega. *(10%)* |
