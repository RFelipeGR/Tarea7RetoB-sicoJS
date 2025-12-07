# 🟨 Reto JS — Hold Shift to Check Multiple Checkboxes  
**Tarea 7: Reto básico JS**

Este proyecto es una reproducción del ejercicio **“Hold Shift to Check Multiple Checkboxes”** del curso **JavaScript30**, creado por Wes Bos.  
El objetivo del reto es implementar, con JavaScript puro (sin librerías), una funcionalidad que permita **seleccionar múltiples checkboxes manteniendo presionada la tecla Shift**, tal como ocurre en aplicaciones de correo o sistemas de archivos.

---

## 📌 ¿En qué consiste el reto?

El usuario puede seleccionar un rango de checkboxes de la siguiente manera:

1. Marca un checkbox.
2. Mantiene presionada la tecla **Shift**.
3. Hace clic en otro checkbox más abajo.
4. Todos los checkboxes entre ambos se seleccionan automáticamente.

Este comportamiento no existe por defecto en HTML, por lo que debe implementarse manualmente usando JavaScript.  
El reto permite practicar manipulación del DOM, eventos y manejo de estado.

---

## 🧠 ¿Qué se busca aprender con este ejercicio?

- Manejar eventos de clic (`click`) en elementos del DOM.
- Detectar cuándo el usuario mantiene presionada la tecla **Shift**.
- Recordar el último checkbox seleccionado.
- Iterar sobre un conjunto de elementos para aplicar una acción (seleccionar un rango).
- Manipular propiedades de los inputs con JavaScript (`checked = true`).

---

## 🛠 Tecnologías utilizadas

- **HTML5** → estructura básica de la interfaz  
- **CSS3** → estilo visual inspirado en el diseño original del reto  
- **JavaScript Vanilla (sin frameworks)** → lógica completa de selección múltiple  

---

## 📂 Estructura del proyecto



/
├── index.html # Página principal con HTML, CSS y JS embebido

└── README.md # Este archivo


---

## 🚀 Cómo ejecutar el proyecto

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/tu-repo.git


Abre el archivo:

index.html


¡Listo! La página funciona directamente en el navegador, sin necesidad de instalación adicional.

🧩 Explicación de la lógica principal

La funcionalidad se basa en:

1️⃣ Seleccionar todos los checkboxes del contenedor:
```bash
const checkboxes = document.querySelectorAll('.inbox input[type="checkbox"]');
```
2️⃣ Guardar el último checkbox marcado:
```bash
let lastChecked;
```

3️⃣ Detectar si el usuario hace clic con Shift presionado:
```bash
if (e.shiftKey && this.checked) {
    // lógica para marcar el rango
}
```

4️⃣ Marcar todos los checkboxes entre el primero y el último seleccionado:
```bash
let inBetween = false;

checkboxes.forEach(checkbox => {
  if (checkbox === this || checkbox === lastChecked) {
    inBetween = !inBetween;
  }
  if (inBetween) {
    checkbox.checked = true;
  }
});
```

5️⃣ Actualizar el último checkbox clickeado:
```bash
lastChecked = this;
```

📸 Vista del proyecto

El diseño replica el mostrado en el reto original:

- fondo amarillo

- caja blanca estilo “inbox”

- checkboxes alineados

- texto que se tacha cuando se selecciona

📚 Fuente original del reto

Este ejercicio pertenece al día 10 del curso JavaScript30:

https://javascript30.com/
