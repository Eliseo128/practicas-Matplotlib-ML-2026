¡Hola! Vamos a trabajar este taller paso a paso. Como docente, he adaptado la guía con ejemplos cotidianos y accesibles para que tus alumnos de preparatoria comprendan la utilidad práctica de la visualización de datos con Matplotlib en VS Code.

---

**Paso 1: Configuración del entorno de trabajo en la terminal**

Abre la terminal en VS Code y ejecuta los comandos según el sistema operativo:

1. **Crear la carpeta del proyecto y entrar en ella:**
```bash
mkdir practica7-ml-matplotlib
cd practica7-ml-matplotlib

```


2. **Crear el entorno virtual `.venv7`:**
* En Windows: `python -m venv .venv7`
* En macOS/Linux: `python3 -m venv .venv7`


3. **Activar el entorno virtual:**
* En Windows (CMD): `.venv7\Scripts\activate`
* En Windows (PowerShell): `.venv7\Scripts\Activate.ps1`
* En macOS/Linux: `source .venv7/bin/activate`


4. **Instalar Matplotlib:**
```bash
pip install matplotlib

```


5. **Seleccionar el intérprete de Python en VS Code:**
* Presiona `Ctrl + Shift + P` (o `Cmd + Shift + P` en macOS).
* Escribe **Python: Select Interpreter**.
* Busca y selecciona la opción que contiene `.venv7` (debe decir `('.venv7': venv)`).



---

**Paso 2: Estructura de carpetas y archivos**

Una vez creados los archivos dentro de la carpeta `practica7-ml-matplotlib`, la estructura en el explorador de VS Code se verá así:

```text
practica7-ml-matplotlib/
│
├── .venv7/                     # Carpeta del entorno virtual
├── practica7a-0777.py          # Ejemplo 1: Calificaciones
├── practica7b-0777.py          # Ejemplo 2: Gastos semanales
├── practica7c-0777.py          # Ejemplo 3: Horas de estudio vs Examen
├── practica7d-0777.py          # Ejemplo 4: Temperatura diaria
└── practica7e-0777.py          # Ejemplo 5: Uso de redes sociales

```

---

**Paso 3: Códigos Python listos para ejecutar**

1. **practica7a-0777.py:** Gráfico de barras: Calificaciones del parcial.
Compara de forma visual el rendimiento en distintas materias.

```python
import matplotlib.pyplot as plt

# Datos del alumno
materias = ['Matemáticas', 'Química', 'Historia', 'Inglés', 'Programación']
calificaciones = [8.5, 7.0, 9.2, 8.8, 9.5]

# Crear el gráfico de barras
plt.figure(figsize=(8, 5))
plt.bar(materias, calificaciones, color='skyblue', edgecolor='black')

# Personalización
plt.title('Calificaciones del Primer Parcial - Alumno 0777')
plt.xlabel('Materias')
plt.ylabel('Calificación (0 - 10)')
plt.ylim(0, 10)
plt.grid(axis='y', linestyle='--', alpha=0.7)

# Mostrar el gráfico
plt.show()

```


2. **practica7b-0777.py:** Gráfico circular: Distribución del gasto semanal.
Muestra la proporción de dinero gastada en diferentes categorías.

```python
import matplotlib.pyplot as plt

# Datos de gastos personales
categorias = ['Transporte', 'Comida/Snacks', 'Materiales', 'Entretenimiento']
gastos = [150, 300, 100, 200]
colores = ['#ff9999', '#66b3ff', '#99ff99', '#ffcc99']

# Crear gráfico de pastel
plt.figure(figsize=(6, 6))
plt.pie(gastos, labels=categorias, autopct='%1.1f%%', startangle=140, colors=colores)

# Título
plt.title('Distribución de Gastos Semanales (Pesos MXN)')

# Mostrar el gráfico
plt.show()

```


3. **practica7c-0777.py:** Gráfico de dispersión: Horas de estudio vs. Resultado.
Visualiza la relación entre el tiempo dedicado al estudio y la nota obtenida (ideal para introducir la idea de correlación en Machine Learning).

```python
import matplotlib.pyplot as plt

# Datos de varios alumnos (Horas vs Calificación)
horas_estudio = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
notas_examen = [5.0, 5.5, 6.0, 6.8, 7.5, 8.0, 8.5, 9.0, 9.8, 10.0]

# Crear gráfico de dispersión (Scatter plot)
plt.figure(figsize=(8, 5))
plt.scatter(horas_estudio, notas_examen, color='purple', s=100, marker='o')

# Personalización
plt.title('Relación entre Horas de Estudio y Nota del Examen')
plt.xlabel('Horas de Estudio Semanales')
plt.ylabel('Calificación Obtención')
plt.grid(True)

# Mostrar gráfico
plt.show()

```


4. **practica7d-0777.py:** Gráfico de líneas: Variación de temperatura durante la semana.
Representa el cambio continuo de una variable a lo largo del tiempo.

```python
import matplotlib.pyplot as plt

# Días y temperaturas registradas
dias = ['Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sábado', 'Domingo']
temperatura = [22, 24, 21, 25, 27, 26, 23]

# Crear gráfico de líneas
plt.figure(figsize=(8, 5))
plt.plot(dias, temperatura, marker='s', color='orange', linewidth=2, linestyle='-')

# Personalización
plt.title('Registro de Temperatura Máxima Semanal (°C)')
plt.xlabel('Días de la semana')
plt.ylabel('Temperatura (°C)')
plt.grid(True, linestyle=':')

# Mostrar gráfico
plt.show()

```


5. **practica7e-0777.py:** Histograma: Distribución del uso diario del teléfono.
Visualiza la frecuencia con la que los alumnos caen en diferentes rangos de tiempo de uso.

```python
import matplotlib.pyplot as plt

# Horas diarias frente al celular de un grupo de 20 alumnos
horas_celular = [2, 3, 3, 4, 4, 4, 5, 5, 5, 5, 6, 6, 7, 7, 8, 8, 9, 10, 11, 12]

# Crear histograma
plt.figure(figsize=(8, 5))
plt.hist(horas_celular, bins=5, color='teal', edgecolor='black', alpha=0.7)

# Personalización
plt.title('Distribución de Horas Diarias de Uso del Celular en el Grupo')
plt.xlabel('Rango de Horas al día')
plt.ylabel('Número de Alumnos')
plt.grid(axis='y', alpha=0.5)

# Mostrar gráfico
plt.show()

```
