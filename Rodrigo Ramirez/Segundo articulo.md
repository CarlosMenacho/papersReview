# Reinforcement Learning: A Tutorial Survey and Recent Advances

## Introducción

![[MDP.png]]

transition probability matrices (TPMs) es el principal problema. En nuestro contexto son las toma de decisiones que puede hacer un robot de los diferentes estados de su entorno. *curse of modeling* y *curse of dimensionality*
**RL es para este tipo de problemas**
**RL is based on discrete-event DP**

---
## Fundamentos de RL

### Componentes principales
1. **Agente:** El tomador de decisiones.
2. **Entorno:** Donde el agente interactúa.
3. **Acciones:** Posibilidades que el agente puede elegir.
4. **Recompensas:** Retroalimentación que guía el aprendizaje.
5. **Estados:** Situaciones observadas del entorno.

### Aplicaciónes y aclaraciones:

![[computer_phile_video.png]]

## **Programación dínamica**
![[programación_dinámica.png]]


---
# Reinforcement Learning with Q-Values

Bellman optimality equation (BOE) -> DP-VI
- In VI, one starts with guessed estimates of the value function and uses the BOE successively to generate e-optimal estimates of the value function—from which the e-optimal policy can be obtained.
Bellman policy equation (BPE) ->DP-PI
- In PI, the general scheme of operation is as follows. One starts with an arbitrary policy. Then the BPE is solved to obtain the value function associated with the policy. The value function is then used to determine a better policy. This continues until the algorithm obtains the optimal policy

![[Q_learning.png]]

### Ventajas de Q-Learning
- Es un método **off-policy**, lo que significa que puede aprender la política óptima incluso mientras sigue otra política.
- No requiere un modelo explícito del entorno.

### Limitaciones
- Ineficiente en espacios de estado grandes o continuos.
- Requiere tablas para almacenar \( Q(s, a) \), lo que puede ser poco práctico.
- El entrenamiento puede ser inestable si los hiperparámetros no están bien ajustados.

---
## Aplicaciones
1. **Juegos:**
   - Ajedrez, Go, videojuegos (ejemplo: Dota 2).
2. **Robótica:**
   - Control de movimientos, navegación autónoma.
3. **Finanzas:**
   - Optimización de carteras, estrategias de trading.
4. **Ingeniería industrial:**
   - Gestión de inventarios, planificación de operaciones.
---
## Referencia
- Artículo: *Reinforcement Learning: A Tutorial Survey and Recent Advances*.
- Autor: Abhijit Gosavi.
- Publicado en: *INFORMS Journal on Computing*.