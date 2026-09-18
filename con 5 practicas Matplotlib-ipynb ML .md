¡Excelente decisión! Trabajar con **Jupyter Notebooks (`.ipynb`)** dentro de **Visual Studio Code** es la forma estándar y más utilizada en el ámbito profesional de Data Science y Machine Learning, ya que permite ejecutar el código por bloques (celdas) y visualizar los gráficos de Matplotlib directamente dentro del editor sin abrir ventanas emergentes.

A continuación, muestro el procedimiento paso a paso adaptado para cuadernos Jupyter.

---

### **Paso 1: Configuración del entorno virtual e instalación de Jupyter**

Abre la terminal en VS Code dentro de la carpeta del proyecto y ejecuta los siguientes comandos:

1. **Entrar a la carpeta del proyecto:**
```bash
cd practica7-ml-matplotlib

```


2. **Asegurarte de que el entorno `.venv7` esté activado:**
* **Windows (CMD):** `.venv7\Scripts\activate`
* **Windows (PowerShell):** `.venv7\Scripts\Activate.ps1`
* **macOS/Linux:** `source .venv7/bin/activate`


3. **Instalar Jupyter, ipykernel y Matplotlib:**
Para poder ejecutar Notebooks dentro del entorno virtual, necesitamos instalar el motor `ipykernel` junto con `jupyter` y `matplotlib`:
```bash
pip install matplotlib jupyter ipykernel

```


4. **Vincular el entorno virtual a Jupyter Notebook:**
Este comando registra tu entorno `.venv7` para que VS Code lo reconozca como un núcleo (*kernel*) de Jupyter disponible:
```bash
python -m ipykernel install --user --name=.venv7 --display-name "Python (.venv7)"

```


5. **Seleccionar el Kernel en VS Code:**
* Abre cualquiera de los archivos `.ipynb` creados en VS Code.
* En la esquina superior derecha del cuaderno, haz clic en **Select Kernel** (o **Seleccionar Kernel**).
* Elige **Python Environments...** y selecciona la opción que dice **Python (.venv7)**.



---

### **Paso 2: Estructura de carpetas y archivos `.ipynb**`

Una vez creados los archivos en el explorador de archivos de VS Code, la estructura quedará de la siguiente manera:

```text
practica7-ml-matplotlib/
│
├── .venv7/                      # Entorno virtual
├── practica7a-0777.ipynb        # Cuaderno 1: Calificaciones del parcial
├── practica7b-0777.ipynb        # Cuaderno 2: Gastos semanales
├── practica7c-0777.ipynb        # Cuaderno 3: Horas de estudio vs Examen
├── practica7d-0777.ipynb        # Cuaderno 4: Variación de temperatura
└── practica7e-0777.ipynb        # Cuaderno 5: Uso del celular

```

---

### **Paso 3: Códigos de Python para las celdas del Notebook**

En cada archivo `.ipynb`, crea una celda de código (Code) e ingresa el código correspondiente. Al ejecutar la celda (presionando `Shift + Enter` o el botón de *Play* a la izquierda de la celda), el gráfico se renderizará e imprimirá inmediatamente debajo.

---

#### **1. `practica7a-0777.ipynb` — Gráfico de Barras: Calificaciones**

> **Explicación didáctica:** Compara de manera visual variables categóricas (materias) contra valores numéricos (calificaciones).

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

# Desplegar gráfico en el notebook
plt.show()

```

---

#### **2. `practica7b-0777.ipynb` — Gráfico Circular: Gastos Semanales**

> **Explicación didáctica:** Permite ver proporciones porcentuales de un total (100%), ideal para finanzas personales.

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

# Desplegar gráfico en el notebook
plt.show()

```

---

#### **3. `practica7c-0777.ipynb` — Gráfico de Dispersión: Horas de Estudio vs. Examen**

> **Explicación didáctica:** Introduce la noción básica de **Machine Learning**: observar si existe una correlación o patrón entre una variable de entrada (horas) y una de salida (nota).

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
plt.ylabel('Calificación Obtenida')
plt.grid(True)

# Desplegar gráfico en el notebook
plt.show()

```

---

#### **4. `practica7d-0777.ipynb` — Gráfico de Líneas: Registro de Temperatura**

> **Explicación didáctica:** Muestra la evolución o tendencia temporal de una variable a lo largo de un período (serie de tiempo).

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

# Desplegar gráfico en el notebook
plt.show()

```

---

#### **5. `practica7e-0777.ipynb` — Histograma: Distribución del Uso del Celular**

> **Explicación didáctica:** Agrupa los datos en rangos (intervalos o *bins*) para analizar cómo se distribuyen las frecuencias en un grupo de datos.

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

# Desplegar gráfico en el notebook
plt.show()

```
