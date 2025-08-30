# Ruta de aprendizaje

## Instalación

Antes de empezar debes instalar el motor de base de datos de su preferencia para empezar. Sin embargo, para efectos de esta pequeña guía, tomaré como punto de partida MySQL o MariaDB. Sin embargo, puedes elegir el de su preferencia.

### En Linux

Para instalar MySQL o MariaDB, escriba la siguiente línea de comando:

```bash
sudo apt install mariadb-server
```

Una vez haya terminado de instalarlo, entonces, proceda a crear el usuario desde el que va a acceder. 

Primero accedemos de esta forma:

```bash
sudo mysql -u root
```

Y luego, creamos el usuario con todos los permisos establecidos para que puedas practicar:

```bash
-- Creas tu usuario con la contraseña:
CREATE USER 'tuusuario'@'localhost' IDENTIFIED BY 'tucontraseña';

-- Estableces los permisos a todas las bases de datos y tablas al usuario 
-- recién creado:
GRANT ALL PRIVILEGES ON *.* TO 'tuusuario'@'localhost';

-- Y finalmente, completas el proceso por medio de:
FLUSH PRIVILEGES;
```

### En Windows

Para Windows, solo debe descargar el instalador desde el [sitio Web oficial](https://mariadb.org/download/?t=mariadb&p=mariadb&r=12.0.2&os=Linux&cpu=x86_64&pkg=tar_gz&i=systemd&mirror=insacom "Descargar motor de base de datos") de MariaDB y seguir las instrucciones.

## Ruta de aprendizaje

### **1️⃣ Evaluar la base que ya tiene**

Ella ya ha trabajado con `SELECT` y subconsultas en filtros. Esto significa que tiene nociones de **consultas simples** y algo de **SQL lógico**.

Lo ideal es partir de ahí, reforzando lo que ya conoce.

---

### **2️⃣ Refuerzo de SELECT y subconsultas**

* **Objetivo:** Recuperar confianza y memoria muscular en SQL.
* **Actividad sugerida:** Mini-proyectos de práctica:

  * Listar datos con filtros y ordenamientos.
  * Agrupar y resumir datos (`GROUP BY`, `HAVING`).
  * Subconsultas en SELECT, FROM y WHERE.
* **Formato:** Puede usar plataformas interactivas como **Mode SQL**, **SQLBolt** o los ejercicios de **LeetCode Database** para no sentirse abrumada con teoría.

---

### **3️⃣ Introducir conceptos intermedios**

* **Joins y relaciones entre tablas**:

  * INNER JOIN, LEFT/RIGHT JOIN, FULL OUTER JOIN.
  * Auto-joins y combinaciones de varias tablas.
* **Funciones agregadas y de ventana**:

  * `SUM`, `AVG`, `COUNT`, etc.
  * Ventanas (`OVER PARTITION BY`) para análisis más avanzado.
* **Práctica:** Usar ejemplos concretos como ventas, usuarios, productos, etc.

---

### **4️⃣ Conceptos de manipulación de datos**

* `INSERT`, `UPDATE`, `DELETE`.
* Transacciones (`COMMIT`, `ROLLBACK`).
* Práctica: Simular escenarios reales (por ejemplo, actualizar stock, registrar ventas).

---

### **5️⃣ Fundamentos de diseño**

* **Claves primarias y foráneas**.
* **Índices básicos** y su impacto.
* **Normalización básica** (1NF, 2NF, 3NF) solo de manera conceptual, suficiente para entender consultas complejas.

---

### **6️⃣ Reforzamiento mediante mini-proyectos**

* Crear una **pequeña base de datos de ejemplo** y aplicar todo lo aprendido:

  * Consultas simples y complejas.
  * Subconsultas, joins, agregaciones.
  * Manipulación de datos.
* Esto consolida aprendizaje sin saturar de teoría.

---

### **7️⃣ Recursos sugeridos**

* **Gratis / interactivo**: SQLBolt, Mode SQL, Khan Academy (SQL Basics).
* **Cursos completos**: Udemy “The Complete SQL Bootcamp” (por ejemplo, de Jose Portilla).
* **Ejercicios prácticos**: LeetCode Database, HackerRank SQL.

---

### **💡 Tips de motivación**

1. **Aprendizaje incremental**: no intentar todo de golpe.
2. **Practicar cada concepto en 10–20 minutos** al día.
3. **Aplicar ejemplos cercanos a su contexto laboral** para que vea el valor inmediato.
4. Celebrar logros pequeños: cada consulta correcta es progreso.
