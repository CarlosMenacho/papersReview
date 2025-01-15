# Deep Reinforcement Learning: A Brief Survey

## Introducción
- The essence of RL is learning through interaction.
	- behaviorist psychology
	- optimal control

En el contexto del **aprendizaje por refuerzo (RL)**, un agente autónomo, controlado por un algoritmo de aprendizaje automático, observa un estado $s_t$ de su entorno en el paso de tiempo $t$. El agente interactúa con el entorno al tomar una acción $a_t$ en el estado $s_t$. Cuando el agente realiza una acción, tanto el entorno como el agente hacen una transición a un nuevo estado, $s_{t+1}$, basado en el estado actual y la acción elegida.

El estado es una **estadística suficiente** del entorno y, por lo tanto, incluye toda la información necesaria para que el agente tome la mejor acción, lo que puede incluir partes del propio agente, como la posición de sus actuadores y sensores. En la literatura de control óptimo, los estados y las acciones a menudo se denotan como $x_t$ y $u_t$, respectivamente.

![[MDP_example.png]]


---

## Métodos principales en DRL

### 1. **Basados en valores**
- Ejemplo: **Deep Q-Network (DQN)**.
- Aprende una función de valor \( Q(s, a) \) que estima la recompensa esperada de una acción \( a \) en un estado \( s \).
- Ventajas:
  - Simple implementación.
  - Efectivo en tareas discretas.
- Desafíos: Escalabilidad a tareas continuas.

### 2. **Basados en políticas**
- Ejemplo: **REINFORCE**.
- Aprende directamente una política \( \pi(a|s) \).
- Ventajas:
  - Apto para espacios de acción continuos.
  - Compatible con gradientes.
- Desafíos: Alta varianza en estimaciones.

### 3. **Métodos actor-crítico**
- Combina los enfoques anteriores:
  - Actor: Aprende la política.
  - Crítico: Aprende la función de valor.
- Ejemplo: **A3C (Asynchronous Advantage Actor-Critic)**.

---

## Aplicaciones
- **Videojuegos:** Ejemplo destacado: AlphaGo, que venció a jugadores humanos en Go.
![[Game_atari_applicattion.png]]
- **Robótica:** Control de movimientos y tareas complejas.
- **Navegación:** Robots y agentes autónomos en entornos desconocidos.

---

## Direcciones futuras
1. **Sample efficiency:**
   - Métodos que requieran menos datos para entrenar.
2. **Escalabilidad:**
   - Adaptar DRL a entornos más complejos y dinámicos.
3. **Sistemas multiagentes:**
   - Coordinación y competencia entre varios agentes.
4. **Transferencia de aprendizaje:**
   - Mejorar la capacidad de reutilizar políticas aprendidas.

---

## Referencia
- Artículo: [Deep Reinforcement Learning: A Brief Survey](https://arxiv.org/abs/1708.05866).
- Autores: Kai Arulkumaran, Marc Peter Deisenroth, Miles Brundage, Anil Anthony Bharath.
- Publicado en: *arXiv*, 2017.
