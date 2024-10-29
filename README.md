# 🌟 DynamicMazeDStarLite: Solucionador de Laberintos Dinámicos con D* Lite

<p align="center">
  <img src="https://raw.githubusercontent.com/GoldHood/DynamicMazeDStarLite/refs/heads/main/DynamicMazeDstarLite_V1.gif" width="300" alt="DynamicMazeDStarLite V1"/>
</p>

<p align="center">
  <strong>Desafía los límites.</strong><br>
  Observa cómo la inteligencia artificial navega y se adapta en tiempo real a laberintos dinámicos.
</p>

---

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg?style=for-the-badge&logo=python)](https://www.python.org/)
[![MIT License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)
[![Open Source Love](https://img.shields.io/badge/Open%20Source-%E2%9D%A4-red.svg?style=for-the-badge)](https://github.com/GoldHood/DynamicMazeDStarLite)
[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg?style=for-the-badge&logo=github)](CONTRIBUTING.md)
[![Status](https://img.shields.io/badge/Status-Active-success.svg?style=for-the-badge)]()

---

## 🚀 Bienvenido a DynamicMazeDStarLite

¿Te has preguntado cómo un algoritmo puede encontrar su camino en un laberinto que cambia constantemente? **DynamicMazeDStarLite** es más que un simple solucionador de laberintos; es una poderosa demostración de cómo la inteligencia artificial y los algoritmos de búsqueda pueden adaptarse y superar obstáculos en tiempo real.

---

## 🔥 ¿Por qué DynamicMazeDStarLite es especial?

- 🧠 **Adaptación en tiempo real:** Nuestro algoritmo D* Lite recalcula y encuentra nuevas rutas al aparecer obstáculos inesperados.
- 🎥 **Visualización interactiva:** Observa cómo el agente navega por el laberinto, ajustándose dinámicamente a los cambios.
- 📚 **Educativo y extensible:** Ideal para aprender sobre algoritmos de búsqueda y para quienes desean experimentar y mejorar el código.
- 🚀 **Próximas mejoras:** Planeamos incorporar nuevas heurísticas y mejorar la eficiencia del algoritmo en futuras versiones.
- 🌐 **Comparación con A\***: Revisa nuestro repositorio del algoritmo A* [aquí](https://github.com/GoldHood/DynamicMazeAstar) y observa las diferencias. D* Lite solo explora nodos nuevos y no busca en toda la memoria como A*, haciéndolo más eficiente.

---

## 🎥 Observa el algoritmo en acción

<p align="center">
  <img src="https://raw.githubusercontent.com/GoldHood/DynamicMazeDStarLite/refs/heads/main/DynamicMazeDstarLite_V1.gif" width="300" alt="DynamicMazeDStarLite V1"/>
</p>

<p align="center">
  <em>El agente azul busca el camino más eficiente hacia la meta dorada, sorteando obstáculos que aparecen en tiempo real.</em>
</p>

---

## 📚 Tabla de Contenidos

- [🚀 Bienvenido a DynamicMazeDStarLite](#-bienvenido-a-dynamicmazedstarlite)
- [🔥 ¿Por qué DynamicMazeDStarLite es especial?](#-por-qué-dynamicmazedstarlite-es-especial)
- [🎥 Observa el algoritmo en acción](#-observa-el-algoritmo-en-acción)
- [⚙️ Instalación](#️-instalación)
- [🕹 Uso](#-uso)
- [🤔 ¿Cómo funciona el algoritmo?](#-cómo-funciona-el-algoritmo)
- [📊 Comparación con A\*: Exploración de Grafos](#-comparación-con-a-exploración-de-grafos)
- [🤝 Contribuciones](#-contribuciones)
- [📬 Contacto](#-contacto)
- [📝 Licencia](#-licencia)
- [🌐 ¡Hazlo viral!](#-¡hazlo-viral)
- [🎯 Próximas versiones](#-próximas-versiones)
- [📄 Detalles del Proyecto](#-detalles-del-proyecto)

---

## ⚙️ Instalación

Asegúrate de tener **Python 3.9+** instalado. Luego, sigue estos pasos:

1. **Clona este repositorio:**

   ```bash
   git clone https://github.com/GoldHood/DynamicMazeDStarLite.git
   cd DynamicMazeDStarLite
   ```

2. **Crea un entorno virtual (opcional pero recomendado):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. **Instala las dependencias necesarias:**

   ```bash
   pip install -r requirements.txt
   ```

---

## 🕹 Uso

1. **Ejecuta el script principal:**

   ```bash
   python dynamic_maze_solver.py
   ```

2. **Disfruta de la simulación:**
   
   Observa cómo el agente navega por el laberinto, adaptándose a los cambios en tiempo real.

---

## 🤔 ¿Cómo funciona el algoritmo?

El algoritmo D* Lite es un algoritmo de búsqueda heurística que encuentra el camino más corto y se adapta a cambios en el entorno en tiempo real. En DynamicMazeDStarLite, hemos implementado D* Lite de la siguiente manera:

- **Heurística:** Utilizamos la distancia de Manhattan como función heurística.
- **Obstáculos dinámicos:** En ciertos pasos, se añaden obstáculos al laberinto, simulando cambios en tiempo real.
- **Replanificación:** Cuando aparece un nuevo obstáculo, el algoritmo recalcula la ruta desde la posición actual, pero solo explora nodos que no están en su memoria, lo cual lo hace mucho más eficiente que A*.

**Visualización del laberinto:**

- 🟩 **Inicio (S):** Punto de partida del agente.
- 🟨 **Meta (G):** Objetivo que el agente debe alcanzar.
- 🔵 **Agente:** Representado como un círculo azul que se mueve por el laberinto.
- 🟥 **Obstáculos:** Paredes y obstáculos dinámicos que el agente debe evitar.
- 🟫 **Camino recorrido:** Celdas que el agente ha visitado.

---

## 📊 Comparación con A\*: Exploración de Grafos

En el algoritmo A*, cada vez que se presenta un cambio dinámico en el laberinto, el agente debe explorar todo el grafo nuevamente como si fuera un nuevo laberinto, lo cual incrementa significativamente el costo computacional. A* no guarda información de la exploración anterior, por lo que no reutiliza los datos obtenidos previamente.

En cambio, **D* Lite** es mucho más eficiente, ya que guarda la información de los grafos explorados previamente. Cuando se presenta un cambio, solo explora los nodos que no han sido explorados o aquellos afectados por el cambio, haciendo que la búsqueda sea más óptima en términos de tiempo y recursos. Esto significa que **D* Lite** no necesita recalcular todo el camino desde cero, lo cual representa una mejora importante en la eficiencia del algoritmo.

En DynamicMazeDStarLite, mostramos cómo el agente recalcula el camino utilizando los grafos explorados anteriormente. Esta capacidad de reutilización es clave para su eficiencia y lo diferencia claramente del comportamiento de A*.

Observa los grafos explorados en las simulaciones y cómo D* Lite evita recalcular toda la ruta, optimizando el proceso.

---

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Sigue estos pasos:

1. **Haz un fork del repositorio.**
2. **Crea una rama nueva:**

   ```bash
   git checkout -b mi-nueva-funcionalidad
   ```

3. **Realiza tus cambios y haz commit:**

   ```bash
   git commit -m "Añadir nueva funcionalidad"
   ```

4. **Envía tus cambios al repositorio remoto:**

   ```bash
   git push origin mi-nueva-funcionalidad
   ```

5. **Abre un Pull Request.**

---

## 📬 Contacto

¿Tienes preguntas o sugerencias? ¡Contáctame!

- **Autor**: Martin Verastegui
- **Email**: martin.verastegui@gmail.com
- **GitHub**: [GoldHood](https://github.com/GoldHood)

---

## 📝 Licencia

Este proyecto está bajo la licencia MIT License.

---

## 🌐 ¡Hazlo viral!

Tu apoyo es esencial para que más personas descubran este proyecto. Aquí tienes cómo puedes ayudar:

- Dale una estrella ⭐ al repositorio.
- Comparte en tus redes sociales:

  > "🚀 Descubre cómo DynamicMazeDStarLite utiliza IA para resolver laberintos dinámicos en tiempo real. ¡Impresionante proyecto open-source! ⭐ https://github.com/GoldHood/DynamicMazeDStarLite #Python #IA #DStarLite #OpenSource"

- Únete a la conversación: Comparte tus ideas y sugerencias.

---

## 🎯 Próximas versiones

¡Esto es solo el comienzo! Estamos trabajando en:

- **Nuevas heurísticas**: Mejoraremos el algoritmo D* Lite con heurísticas más eficientes.
- **Visualizaciones avanzadas**: Incluiremos gráficos y estadísticas detalladas sobre el rendimiento del algoritmo.

---

## 📄 Detalles del Proyecto

```
# -----------------------------------------------------
# Proyecto: DynamicMazeDStarLite
# Autor: Martin Verastegui
# Fecha: 29 de octubre de 2024
# Licencia: MIT License
# Descripción: Solucionador de laberintos dinámicos utilizando el algoritmo D* Lite en Python.
# Repositorio: https://github.com/GoldHood/DynamicMazeDStarLite
# -----------------------------------------------------
```

<p align="center"> <i>¡Gracias por ser parte de DynamicMazeDStarLite!</i> <br> <strong>✨ Juntos, hagamos que la inteligencia artificial sea accesible para todos. ✨</strong> </p>
