[README.md.md](https://github.com/user-attachments/files/34056044/README.md.md)
# Desafío Académico: Método de Gradientes Conjugados Precondicionado (MAT-242)

## Información del Estudiante
* **Estudiante:** Javier Marco Garzon Canedo
* **Carrera:** Informática
* **Mención:** Inteligencia Artificial y Ciencia de Datos
* **Sigla Asignatura:** MAT-242 (Métodos Numéricos)
* **Docente / Institución:** Universidad Mayor de San Andrés (UMSA), Facultad de Ciencias Puras y Naturales

---

## 1. Descripción del Proyecto
Este repositorio contiene el desarrollo e implementación del **Método de Gradientes Conjugados Precondicionado (GCP)** aplicado a la optimización de riesgo en carteras de inversión ($n \ge 4$), fundamentado en el artículo científico del Dr. Porfirio Suñagua S.:

> **Suñagua S., P. (2020).** *Método de Gradientes Conjugados Precondicionado*. Revista Boliviana de Matemática UMSA, 04, 2-7.

### Enfoque de la Mención (Inteligencia Artificial y Ciencia de Datos)
El modelo resuelve las condiciones necesarias de primer orden (Karush-Kuhn-Tucker) para la minimización de varianza cuadrática de Markowitz en un portafolio de 4 activos financieros:
1. $x_1$: Acciones Tecnológicas (Renta Variable Global)
2. $x_2$: Debentures Corporativos (Renta Fija Privada)
3. $x_3$: Bonos Soberanos / Estatales
4. $x_4$: Liquidez y Fondos Monetarios

El sistema lineal simétrico y definido positivo $Ax = b$ se evalúa numéricamente bajo tres escenarios: **Ideal**, **Bajo Estrés Financiero** y **Mal Condicionado**.

---

## 2. Arquitectura de Software
La aplicación web es una *Single Page Application* (SPA) reactiva e interactiva desarrollada sin dependencias complejas de compilación:
* **Interfaz de Usuario:** HTML5 nativo (codificación UTF-8 pura), Bootstrap 5.3.2 y Bootstrap Icons.
* **Motor Matemático:** `math.js` (v11.8.0) para operaciones matriciales directas, descomposición LU/Cholesky, cálculo del número de condición y normas vectoriales.
* **Renderizado Matemático:** HTML5 semántico con tablas estilizadas para corchetes de matrices y notación UTF-8.

---

## 3. Instrucciones de Instalación y Ejecución Local

### Prerrequisitos
No requiere entornos de ejecución de backend (Node.js, Python, PHP, etc.). Solo se necesita un navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge o Safari).

### Pasos de Ejecución
1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/javiergarzon/MAT242-GCP-Finanzas.git
   cd MAT242-GCP-Finanzas
   ```

2. **Abrir la aplicación web:**
   Haga doble clic sobre el archivo `index.html` o ejecútelo desde la terminal:
   * **En Linux / macOS:**
     ```bash
     open index.html
     ```
   * **En Windows:**
     ```cmd
     start index.html
     ```

---

## 4. Estructura del Repositorio
```text
MAT242-GCP-Finanzas/
│
├── index.html          # Aplicación web interactiva completa (10 Módulos)
└── README.md           # Documentación técnica, arquitectura e instrucciones de uso
```

---

## 5. Módulo de Pruebas y Calidad de Software (QA)
La aplicación web integra un módulo de control de calidad para probar automáticamente:
1. **Prueba de Carga de Escenarios:** Verificación de matrices en los escenarios Ideal, Estrés y Mal Condicionado.
2. **Validación de Matriz Inválida:** Detección y notificación al usuario cuando la matriz no es simétrica ($A \ne A^T$) o no es definida positiva.
3. **Edición Dinámica:** Modificación interactiva de coeficientes $a_{ij}$ con recálculo instantáneo.
4. **Prueba Comparativa GCP vs GC:** Verificación de aceleración de convergencia con el Precondicionador de Jacobi en escenarios con elevado número de condición ($\kappa(A) = 390.50$).

---

## 6. Enlaces de Entrega
* **Página Web Funcional:** `https://javiergarzon.github.io/MAT242-GCP-Finanzas/`
* **Repositorio de Código Fuente:** `https://github.com/javiergarzoncanedo-wq/javiergarzon-MAT242-GCP-Finanzas/settings/pages`
