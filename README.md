# 🎰 Ruleta React Promocional – Tec Store Argentina

Aplicación web promocional creada para ofrecer premios a clientes mediante una ruleta interactiva. El acceso está validado por código y número de pedido, y toda la lógica de participación se gestiona automáticamente con Google Sheets como base de datos.

> ✅ En uso real desde 2024  
> 🎯 Desarrollada específicamente para campañas de fidelización y sorteos post-compra en **Tec Store Argentina**

---

## 🎯 ¿Para qué fue creada?

Este proyecto nació como una solución interna para Tec Store, con el objetivo de:

- Incentivar a los clientes a participar de promociones luego de una compra
- **Obtener visibilidad orgánica en redes sociales**: para participar, el cliente debe subir una historia mencionando a la tienda, lo cual es requisito para acceder a la ruleta
- Gamificar la experiencia de post-venta
- Eliminar la participación duplicada o no válida
- Centralizar el control de premios y participantes

De esta forma no solo mejoramos la interacción con el cliente, sino que también **aumentamos el alcance y la presencia de la marca** de forma automatizada y natural.

---

## 🛠️ Cómo funciona

1. El cliente accede a la página de la ruleta
2. Ingresa dos datos:
   - Código de participación: `RXXXX` (se genera automáticamente desde Google Sheets usando los últimos 4 dígitos del número de WhatsApp o similar)
   - Número de pedido: `PXXXXXX` (se asigna al momento de la compra)
3. El sistema valida los datos contra Google Sheets:
   - ✅ Si es válido y no participó aún → se habilita la ruleta
   - ❌ Si ya participó o los datos no coinciden → se rechaza
4. El cliente puede girar la ruleta una sola vez
5. El resultado del giro (premio o "seguí participando") se guarda en otra hoja de Google Sheets junto al número de pedido
6. Si ya participó, no puede volver a hacerlo

---

## 🧪 Ejemplo visual

<p align="center">
  <img src="./images/ruleta-demo.gif" width="600" />
</p>

---

## 📊 Control de datos (Google Sheets)

Usamos Google Sheets como base de datos dinámica para leer y escribir información.

Sugerencias de capturas para incluir en este README:

1. 📋 **Hoja de Participantes**
   - Columnas: `Código`, `Pedido`, `Participó`, `Premio`, `Fecha`
   - Se ve reflejado cada intento y su resultado

2. 🎁 **Hoja de Premios Configurados**
   - Donde se definen los premios posibles y sus probabilidades

3. 🥳 **Pantalla de Felicitaciones**
   - Con nombre del cliente y premio ganado

---

## ⚙️ Tecnologías utilizadas

- `React` – SPA moderna
- `Vite` – Build rápido
- `Tailwind CSS` – Estilo responsivo
- `Chart.js` + `canvas-confetti` – Ruleta con animación + confetti
- `Google Sheets API` – Para validar y registrar participaciones en tiempo real
- `Node.js` (backend de validación opcional)

---

## 🚧 Lógica implementada

- Validación en tiempo real de códigos `RXXXX` y pedidos `PXXXXXX`
- Lógica de participación única por cliente
- Animación con probabilidades por premio
- Sonido de ruleta + sonido de victoria
- Registro automático del resultado
- Desactivación del botón luego de girar

---

## 🔐 Código

El código fuente no está disponible públicamente. Este proyecto está en uso privado por razones de seguridad, pero su funcionamiento está documentado en este repositorio.

---

> 💬 *“Transformamos un simple sorteo en una experiencia divertida, viralizable y controlada para nuestros clientes.”*
