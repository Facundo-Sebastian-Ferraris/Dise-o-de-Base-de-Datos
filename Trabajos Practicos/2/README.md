# 📋 **Trabajo Práctico N°2 - Diseño de Bases de Datos** 🗂️  

## **📌 Consignas**  

### **1️⃣ Pregunta Teórica**  

🔹 **¿Cuál es el propósito de definir dependencias funcionales?**  
📝 Justificar utilizando ejemplos concretos.  

---

### **2️⃣ Álgebra Relacional**  

🔹 Dada una relación **R** sobre un esquema **R**, con la propiedad **XY** (donde **X ⊆ R** y **Y ⊆ R**).  
❓ **¿Cómo expresarías esta dependencia usando operadores del álgebra relacional?**  

---

### **3️⃣ Análisis de Dependencias Funcionales**  

🔹 Dada la siguiente relación **R(A, B, C, D, E)**:  

| A  | B  | C  | D  | E  |  
|----|----|----|----|----|  
| A1 | B1 | C1 | D1 | E1 |  
| A1 | B2 | C2 | D2 | E1 |  
| A2 | B1 | C3 | D3 | E1 |  
| A2 | B1 | C4 | D3 | E1 |  
| A3 | B2 | C5 | D1 | E1 |  

❓ **¿Cuáles de estas dependencias satisface R?**  

- [`A → D`](./3-a.md) ❌
- [`AB → D`](./3-b.md)  ✅
- [`C → BDE`](./3-c.md) ✅
- [`E → A`](./3-d.md) ❌
- [`A → E`](./3-e.md)  ✅

### **4️⃣ Algoritmo de Verificación de DF**  

🔹 **Diseñar un algoritmo** para comprobar si una dependencia funcional **X → Y** es válida en una relación **r** con esquema **R**.  

---

### **5️⃣ Algoritmo de Deducción de DF**  

🔹 **Diseñar un algoritmo** para verificar si una dependencia funcional **se deduce** de un conjunto **F** de DFs.  

---

### **6️⃣ Aplicación del Algoritmo**  

🔹 Dado el conjunto **F = {AB → C, B → D, CD → E, CE → GH, G → A}**, demostrar si:  
✅ **F ⊨ AB → E**  
✅ **F ⊨ BG → C**  
✅ **F ⊨ AB → G**  

---

### **7️⃣ Modelado de Base de Datos**  

🔹 Una **compañía estudiantil** organiza cursos con las siguientes características:  

- 📚 Cursos dictados por **uno o más profesores** (de distintas universidades).  
- ⏳ Cada curso tiene **duración en horas** y puede incluir **uno o más temas**.  
- 👨🎓 **Alumnos y docentes** pueden asistir.  
- 💰 **Precio variable** (diferente para alumnos/docentes).  
- 💵 **Profesores reciben un % del total recaudado**.  

#### **Partes a resolver:**  

a. **Modelo Entidad-Relación** (justificar relaciones y funcionalidades).  
b. **Establecer dependencias funcionales** relevantes.  

---

### **8️⃣ Cubrimientos Minimales**  

🔹 **¿Cuál es el objetivo de definirlos?**  
📝 Explicar los pasos para obtenerlos.  

---

### **9️⃣ Ejercicio de Cubrimiento No Redundante**  

🔹 Encontrar un **cubrimiento no redundante** para:  
**G = {A → C, AB → C, C → DI, CD → I, EC → AB, EI → C}**  

### 🔟 **Reducción de Dependencias Funcionales**

**G = {A→C; AB→DE; AB→CDI; AC→J}**  
📌 **Consigna:**  

- Reducir a izquierda y derecha el conjunto G  
*(Simplificar lados izquierdos y derechos de las DFs)*

---

### 1️⃣1️⃣ **Cubrimiento Minimal y Claves**  

**R(ABCDEFI)** con **G = {A→C; AB→C; C→DI; CD→I; EC→AB; EI→C}**  
📌 **Consignas:**  
a. Encontrar cubrimiento minimal para G  
b. Identificar **todas las claves** de R  

---

### 1️⃣2️⃣ **Anomalías en Esquema Relacional**

**R(A,M,C,D,J,L,N,U)** con **F = {A→MCD, D→J, L→N, AL→U}**  
📌 **Consigna:**  
Mostrar ejemplos concretos de:

- Anomalía de **inserción**  
- Anomalía de **borrado**  
- Anomalía de **actualización**  

---

### 1️⃣3️⃣ **Propiedades de Descomposición**  

📌 **Consignas:**  

1. Listar propiedades deseables en descomposiciones  
2. Explicar **por qué descomponemos** esquemas  

---

### 1️⃣4️⃣ **Descomposición sin Pérdida (JSP)**  

**R(ABCD)** con **F = {A→B, C→D}**  
📌 **Consigna:**  
Probar que existe una descomposición con **Join Sin Pérdida**  

---

### 1️⃣5️⃣ **Normalización a 3FN**  

**R(#Estudiante, Nombre, Fecha_Nacimiento, Edad, Curso, Grado, Semestre, Departamento, Supervisor)**  
📌 **Consignas:**  
a. Descomposición que preserve DFs en 3FN  
b. Descomposición que cumpla **3FN + JSP + Preservación DFs**  

---

### 1️⃣6️⃣ **Problema Complejo: Inversora**  

**R(A,O,S,C,I,D)** con **F = {S→D, I→A, IS→C, A→O}**  
📌 **Consignas:**  
a. **Parte I - Esquema Original:**  
   i. Encontrar clave  
   ii. ¿Cuántas claves existen? Justificar  
   iii. Descomposición en **FNBC**  
   iv. Descomposición en **3FN-JSP-Preservación DFs**  

b. **Parte II - Descomposición R1(ISCD), R2(IAO):**  

- Analizar redundancias y anomalías  

c. **Parte III - Otra Descomposición:**  

- Verificar si tiene JSP  

d. **Parte IV - Descomposición Alternativa:**  
   i. Cubrimientos minimales por esquema  
   ii. Cubrimiento minimal unificado  
   iii. ¿Preserva DFs?  

---

### 1️⃣7️⃣ **Códigos Postales y Ciudades**  

**R(Ciudad, Dirección, Código_Postal)** con **F = {Ciudad Dirección→CP, CP→Ciudad}**  
📌 **Consignas:**  
a. Descomposición en **3FN-JSP-Preservación DFs**  
b. Probar afirmación:  

- ¿CP→Ciudad implica Ciudad Dirección→CP?  

---

### 1️⃣8️⃣ **Sistema Educativo**  

**R(CTHRSG)** con **F = {C→T, HR→C, HT→R, CS→G, HS→R}**  
📌 **Consignas:**  
a. Determinar **claves candidatas**  
b. Descomposición en **FNBC**  
c. ¿La descomposición preserva DFs?  

---

### 1️⃣9️⃣ **Ejercicio Integrador Avanzado**  

**R=(A,B,C,D,E,F,G)** con **F={D→EA, AB→D, F→CE, B→C, DE→A, CB→E}**  
📌 **Consignas:**  
a. Cubrimiento minimal **G** (detallar pasos)  
b. Claves candidatas y **forma normal** del esquema  
c. Descomposición en **FNBC + JSP**  
   i. ¿Preserva DFs? Demostrar  
d. Analizar forma normal de **D=(ABD,ABE,FCE,ABFG)**  
e. Verificar **JSP y preservación DFs**  
f. Nueva descomposición en **3FN**  
   i. ¿Garantiza JSP?  

---

### 2️⃣0️⃣ **Mega-Desafío Normalización**  

**R=(A,B,C,D,E,F,G,H,I)** con **F={AB→CD, AC→BD, A→DE, CD→F, G→H, H→G, GH→I}**  
📌 **Consignas:**  
a. Cubrimiento minimal (paso a paso)  
b. Claves candidatas y forma normal  
c. Descomposición en **3FN + JSP + Preservación DFs**  
   i. ¿Está en FNBC?  
d. Analizar forma normal de **D=(ABCEF,ACDFGI,GHI)**  
e. Verificar **JSP y preservación DFs**  
f. Si no cumple FNBC, proponer nueva descomposición óptima  
   i. ¿Preserva DFs?  
