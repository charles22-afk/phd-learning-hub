# Hub de Aprendizaje Técnico & Investigación Aplicada

Repositorio personal de recursos, enlaces de acceso rápido, notas conceptuales y seguimiento del plan de estudio de 16 semanas.

---

## 1. Calendario Semanal de Estudio (15 h / semana)

| Día | Bloque Temático | Foco Técnico Principal | Horas |
| :--- | :--- | :--- | :--- |
| **Lunes** | **Pilar A:** Software & Tools | Terminal, Git, modularidad, entornos (`venv`/`uv`) | 3 h |
| **Martes** | **Pilar B:** Simulación & Control | Arrays `numpy`, EDOs con `scipy`, modelos dinámicos | 3 h |
| **Miércoles** | **Pilar C:** Datos & Series Temporales | SCADA, `pandas`/`polars`, filtros IEC, métricas físicas | 3 h |
| **Jueves** | **Pilar A:** Software & Tools | Clases, *debugging*, estructura de paquetes y pruebas | 3 h |
| **Viernes** | **Pilar B:** Simulación & Control | Lazos de control (pitch/par), espacio de estados, estabilidad | 3 h |

---

## 2. Repositorio de Recursos por Pilar

### Pilar A: Herramientas, Entorno & Buenas Prácticas
* **The Missing Semester of Your CS Education (MIT):**
  * Web oficial: [missing.csail.mit.edu](https://missing.csail.mit.edu/)
  * Temas clave: Shell (Lecc. 1-2), Git (Lecc. 6), Debugging/Profiling (Lecc. 8).
* **Software Carpentry - Programming with Python:**
  * Lecciones: [swcarpentry.github.io/python-novice-inflammation](https://swcarpentry.github.io/python-novice-inflammation/)
* **Practical Python Programming (David Beazley):**
  * Curso completo: [dabeaz-course.github.io/practical-python](https://dabeaz-course.github.io/practical-python/)

### Pilar B: Física, Control & Dinámica de Sistemas
* **Canal de Steve Brunton (Universidad de Washington):**
  * Canal de YouTube: [youtube.com/@SteveBrunton](https://www.youtube.com/@SteveBrunton)
  * Listas prioritarias: *Control Bootcamp*, *Dynamical Systems*, *SVD & POD*.
* **Brian Douglas - Control Systems Lectures:**
  * Canal de YouTube: [youtube.com/@BrianBDouglas](https://www.youtube.com/@BrianBDouglas)
* **Libros de Consulta:**
  * *A Primer on Scientific Programming with Python* (H. P. Langtangen).
  * *Data-Driven Science and Engineering* (Brunton & Kutz) – Capítulos 1 y 2.

### Pilar C: Series Temporales, Estadística & Datos Eólicos
* **Forecasting: Principles and Practice (Hyndman & Athanasopoulos):**
  * Libro en línea gratuito: [otexts.com/fpp3](https://otexts.com/fpp3/)
* **An Introduction to Statistical Learning (ISLP):**
  * Descarga en PDF: [statlearning.com](https://www.statlearning.com/)
* **Datasets de Práctica SCADA:**
  * Kelmarsh Wind Farm Data (Zenodo / Cubico): [doi.org/10.5281/zenodo.3980382](https://doi.org/10.5281/zenodo.3980382)
  * NREL OpenFAST & Modelos de referencia: [github.com/OpenFAST/openfast](https://github.com/OpenFAST/openfast)

---

## 3. Checklist de Hitos por Ciclo

### Ciclo 1: Pipeline Funcional Mínimo (Semanas 1-4)
- [ ] **Semana 1:** Configurar terminal, Git local y entorno virtual reproducible.
- [ ] **Semana 2:** Vectorizar cálculos de $C_p(\lambda, \beta)$ con `numpy` (eliminar bucles `for`).
- [ ] **Semana 3:** Cargar y limpiar datos SCADA de 10 minutos (Kelmarsh) con `pandas`.
- [ ] **Semana 4:** Estructurar el código en módulos (`src/`) y ejecutar desde terminal.

### Ciclo 2: Dinámica Temporal & Métricas (Semanas 5-8)
- [ ] **Semana 5:** Integrar EDOs con `scipy.integrate.solve_ivp` para el tren de potencia.
- [ ] **Semana 6:** Implementar ventanas móviles (`rolling`) para cálculo de turbulencia ($TI$).
- [ ] **Semana 7:** Añadir pruebas unitarias simples (`assert`) para rangos físicos admisibles.
- [ ] **Semana 8:** Ajustar curva de potencia logística y graficar residuos frente a velocidad.

### Ciclo 3: Lazos de Control & Diagnóstico de Residuos (Semanas 9-12)
- [ ] **Semana 9:** Diseñar lazo cerrado de control de pitch con `python-control`.
- [ ] **Semana 10:** Evaluar respuesta a ráfagas de viento y verificar estabilidad en espacio de estados.
- [ ] **Semana 11:** Desglosar métricas (RMSE, MAE, MBE) en *bins* de viento de 1 m/s.
- [ ] **Semana 12:** Redactar justificación física de los desvíos en la zona de transición par/pitch.

### Ciclo 4: Modelos Predictivos & Portafolio (Semanas 13-16)
- [ ] **Semana 13:** Entrenar modelo multivariable regularizado (Ridge/Lasso) con `scikit-learn`.
- [ ] **Semana 14:** Implementar validación cruzada ($k$-fold) protegiendo el orden temporal.
- [ ] **Semana 15:** Redactar `README.md` técnico con figuras y conclusiones para la tesis.
- [ ] **Semana 16:** Dejar repositorio público/limpio con `pyproject.toml` para consulta externa.

---

## 4. Notas Rápidas & Trucos de Consola

```bash
# Crear y activar entorno virtual
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
# .venv\Scripts\activate   # Windows

# Git: flujo diario básico
git status
git add .
git commit -m "feat: implementado cálculo de residuos por tramos de viento"
git push origin main
