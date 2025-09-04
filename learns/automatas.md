# 📚 Ruta de Aprendizaje: Matemática Aplicada al Cómputo

## 🔹 1. Conjuntos y funciones (la base de todo)

👉 **Idea para niño:** imagina cajas con pelotas de colores.

* Conjunto = una caja con pelotas.
* Función = una regla que te dice qué pelota sacar o cambiar.

**Formal:**

* Un conjunto es una colección bien definida de elementos:

  $$
  A = \{1, 2, 3\}, \quad B = \{a, b, c\}
  $$
* Una función es una correspondencia:

  $$
  f : A \to B, \quad f(1) = a, f(2) = b, f(3) = c
  $$

**Aplicado:** en JSON, el conjunto son las **claves** y la función es la **operación para obtener el valor**.

---

## 🔹 2. Producto cartesiano (las coordenadas mágicas)

👉 **Idea para niño:** combina todas las camisetas (rojas, azules) con todos los pantalones (cortos, largos).

**Formal:**

$$
A = \{rojo, azul\}, \quad B = \{corto, largo\}
$$

$$
A \times B = \{(rojo, corto), (rojo, largo), (azul, corto), (azul, largo)\}
$$

**Aplicado:** cada par $(estado, símbolo)$ es como decir:
👉 "Si estoy en este objeto JSON y veo esta clave, ¿a dónde voy?"

---

## 🔹 3. Autómatas finitos (máquinas con memoria cero)

👉 **Idea para niño:** imagina un robot que está en un laberinto de 3 habitaciones. Cada vez que ve una puerta con una letra, sabe a qué cuarto ir.

**Formal:**
Un autómata es una 5-tupla:

$$
M = (Q, \Sigma, \delta, q_0, F)
$$

* $Q$ = estados
* $\Sigma$ = símbolos de entrada
* $\delta: Q \times \Sigma \to Q$ = función de transición
* $q_0$ = estado inicial
* $F$ = estados finales

**Aplicado:** perfecto para recorrer JSON **planos** (sin anidamiento).

---

## 🔹 4. Autómatas con pila (máquinas con memoria)

👉 **Idea para niño:** el robot ahora tiene una mochila (pila). Puede meter cosas y sacarlas para no perderse.

**Formal:**

$$
M = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)
$$

* $\Gamma$ = símbolos de pila
* $\delta: Q \times \Sigma \times \Gamma \to Q \times \Gamma^*$

**Aplicado:** aquí ya podemos recorrer **JSON anidados**, porque la pila recuerda en qué nivel estamos.

---

## 🔹 5. Gramáticas formales (el idioma de las máquinas)

👉 **Idea para niño:** igual que armar frases con sujeto + verbo + objeto.

**Formal:**
Una gramática es:

$$
G = (V, \Sigma, R, S)
$$

* $V$ = variables (no terminales)
* $\Sigma$ = alfabeto (terminales)
* $R$ = reglas
* $S$ = símbolo inicial

**Aplicado:** el JSON completo es un **lenguaje formal** descrito por una gramática.

---

## 🔹 6. Aplicación práctica al JSON

👉 **Idea para niño:** caminar por un árbol de cajas dentro de cajas, siempre con un mapa (autómata) y una mochila (pila).

**Formal:**

* Entrada = lista de índices (claves).
* Máquina = autómata con pila.
* Salida = valor encontrado o error.

**Aplicado directo:** implementar acceso no recursivo a datos anidados.

---

# 🚀 Plan de estudio progresivo

1. **Semana 1-2** → Conjuntos y funciones (intuición + notación).
2. **Semana 3** → Producto cartesiano + tablas de transición.
3. **Semana 4** → Autómatas finitos (tablas y diagramas).
4. **Semana 5-6** → Autómatas con pila (ejemplos con paréntesis balanceados).
5. **Semana 7** → Gramáticas formales (desde expresiones hasta JSON).
6. **Semana 8+** → Construcción del parser no recursivo para JSON.

