# Descrição Geral

Este projeto é uma experiência imersiva em realidade virtual (VR) criada com a biblioteca **A-Frame**. O cenário apresenta uma simulação de um campo de futebol com interação de elementos 3D. A experiência inclui:

- **Uma bola de futebol:** Interativa, pode ser movida e resetada.
- **Um gol de futebol:** Destino da bola.
- **Dois botões:** Um vermelho que movimenta a bola e um azul que reseta a posição da bola.
- **Um computador da NASA:** Item decorativo no cenário.
- **Chão com textura de gramado:** Representa o campo.

# Funcionalidades

1. **Botão Vermelho:** 
   - Quando pressionado, faz a bola rolar na direção do gol.
   - Se a bola entra no gol, um efeito sonoro de gol é reproduzido.

2. **Botão Azul:**
   - Reseta a posição e a rotação da bola para os valores iniciais.

3. **Interatividade:**
   - O movimento da bola é gerenciado por um componente customizado `move-ball`.
   - A reposição da bola é gerenciada pelo componente `reset-ball`.

# Componentes Personalizados

## `move-ball`
- Gerencia o movimento da bola.
- Atributos configuráveis:
  - **`limitX`:** Limite na direção X para o movimento.
  - **`minZ`:** Limite mínimo na direção Z.
  - **`initialSpeed`:** Velocidade inicial da bola ao ser acionada.
  - **`deceleration`:** Taxa de desaceleração da bola.
- A bola para ao atingir os limites definidos ou quando a velocidade chega a zero.

## `reset-ball`
- Reseta a posição e rotação da bola.
- Atribui valores iniciais ao ser acionado por um clique.

# Assets Utilizados

- **Texturas e Modelos:**
  - `green-fake-grass-background.jpg`: Textura do gramado.
  - `soccer_ball.glb`: Modelo 3D da bola de futebol.
  - `soccer_goal.glb`: Modelo 3D do gol de futebol.
  - `old_nasa_style_computer_console.glb`: Modelo 3D do computador NASA.
- **Efeitos Sonoros:**
  - `goal_sound_effect.mp3`: Reproduzido ao marcar um gol.
