# 📡 Código Hamming (7,4) — Comunicaciones Digitales

## 📖 Descripción

Este repositorio presenta el desarrollo de una práctica de laboratorio de **Comunicaciones Digitales**, enfocada en el estudio y aplicación del **código Hamming (7,4)** para la detección y corrección de errores en sistemas de comunicación digital.

Durante la práctica se identificaron los bits de información y los bits de paridad, se organizaron dentro de una palabra de 7 bits y se utilizaron operaciones **XOR** para calcular y verificar las condiciones de paridad. Finalmente, se obtuvo el **síndrome de error** para comprobar la validez de la palabra codificada.

---

## 🎯 Objetivos

* 🔢 Identificar los bits de información y los bits de paridad del código **Hamming (7,4)**.
* 📍 Ubicar correctamente los bits dentro de la palabra codificada.
* 🔄 Calcular los bits de paridad mediante operaciones **XOR**.
* 🧮 Obtener la palabra codificada de **7 bits**.
* 🔎 Verificar el código mediante comprobaciones de paridad.
* 📊 Obtener e interpretar el **síndrome de error**.
* 🛡️ Comprender la utilidad del código Hamming en la detección y corrección de errores de un solo bit.

---

## 🧠 Fundamento

El **código Hamming** agrega bits de paridad a los datos originales para permitir la detección y corrección de errores durante la transmisión de información digital.

En el código **Hamming (7,4)**:

* 📥 **4 bits** corresponden a la información.
* 🔢 **3 bits** corresponden a paridad.
* 📦 Se obtiene una palabra codificada de **7 bits**.
* 📍 Los bits de paridad se ubican en las posiciones **1, 2 y 4**.
* 🔄 Se utiliza **paridad par**.
* ⚡ Las operaciones **XOR** permiten calcular y comprobar los bits de paridad.

---

## 🔬 Metodología

### 1️⃣ Asignación de las palabras

Para la práctica se utilizó el código estudiantil **1401660**, a partir del cual se establecieron las palabras binarias:

```text
Word A = 0100
Word B = 0100
```

Ambas palabras contienen **4 bits de información**, por lo que se utilizó el código Hamming (7,4).

---

### 2️⃣ Distribución de bits

La estructura del código Hamming (7,4) se organiza de la siguiente manera:

| 📍 Posición |  1 |  2 |  3 |  4 |  5 |  6 |  7 |
| ----------- | -: | -: | -: | -: | -: | -: | -: |
| 🔹 Tipo     | P0 | P1 | D0 | P2 | D1 | D2 | D3 |

Los bits de paridad se encuentran en las posiciones correspondientes a las potencias de 2:

**1, 2 y 4**

mientras que las posiciones restantes contienen los bits de información.

---

### 3️⃣ Cálculo de los bits de paridad

Para determinar los valores de **P0, P1 y P2** se utilizaron operaciones XOR, manteniendo una condición de **paridad par**.

Los grupos de comprobación utilizados fueron:

```text
P0 → posiciones 1, 3, 5, 7
P1 → posiciones 2, 3, 6, 7
P2 → posiciones 4, 5, 6, 7
```

Cada grupo fue evaluado mediante operaciones XOR para determinar los valores correspondientes de los bits de paridad.

---

## 📊 Resultados

### 💾 Palabra codificada

Para la palabra de entrada:

```text
0100
```

se obtuvo la siguiente palabra codificada mediante Hamming (7,4):

```text
0101010
```

El mismo resultado se obtuvo para **Word A** y **Word B**, debido a que ambas palabras de entrada tienen el mismo valor binario.

---

### 🔎 Verificación de paridad

Se realizaron nuevamente las comprobaciones de los tres grupos de paridad:

| 🔢 Bit | 📍 Posiciones verificadas | ✅ Resultado XOR |
| ------ | ------------------------- | --------------: |
| P0     | 1, 3, 5, 7                |               0 |
| P1     | 2, 3, 6, 7                |               0 |
| P2     | 4, 5, 6, 7                |               0 |

Los tres grupos obtuvieron un resultado **0**, indicando que cumplen con la condición de paridad par.

---

### 🧮 Síndrome de error

El resultado de las comprobaciones fue:

```text
P2 P1 P0
 0  0  0
```

Por lo tanto:

**Síndrome = `000`**

Un síndrome igual a `000` indica que **no se detectaron errores** en la palabra codificada durante la verificación.

---

## 📌 Conclusiones

✅ Se comprendió el procedimiento de codificación mediante **Hamming (7,4)** y la distribución de los bits de información y paridad.

✅ Las operaciones **XOR** permitieron calcular y verificar correctamente los bits de paridad utilizando una condición de paridad par.

✅ Para la palabra de entrada `0100` se obtuvo la palabra codificada **`0101010`**.

✅ Las comprobaciones de los tres grupos de paridad produjeron resultados iguales a **0**.

✅ El **síndrome `000`** confirmó que no se detectaron errores en la palabra codificada durante el proceso de verificación.

🔎 La práctica permitió comprender cómo el código Hamming puede utilizarse para **identificar y corregir errores de un solo bit**, contribuyendo a la confiabilidad de la transmisión de información digital.

---

## 👤 Autor

**Harol Felipe Riveros Sierra**

**Código:** 1401660

### Docente

**Ing. José de Jesús Rugeles Uribe**

* **Programa:** Ingeniería en Telecomunicaciones
* **Asignatura:** Comunicaciones Digitales
* **Universidad:** Universidad Militar Nueva Granada
* **Periodo:** 2026-2

---

