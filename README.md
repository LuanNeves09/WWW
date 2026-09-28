# 🚀 Guia de Execução - Linha de Produção Virtual & SCADA

Este documento traz as instruções necessárias para clonar, configurar e rodar a simulação da célula de manufatura integrada (Arduino UNO + Node-RED + Godot/OIP + Mosquitto MQTT).

---

## 🛠️ Requisitos do Sistema

Certifique-se de ter instalado no computador:
* **Mosquitto MQTT Broker** (Servidor rodando na porta padrão `1883`).
* **Node-RED** com os módulos baixados (`Paleta ➔ Gerenciar Paleta`):
  * `node-red-dashboard` ()
  * `node-red-node-serialport`
* **Arduino IDE** (com driver da placa Arduino instalado).
* **Godot Engine 3.x / Open Industry Project (OIP)**.


---
## Tópicos:

- belt_speed - FloatLE - Velocidade da esteira principal (0.0 a 1.0).
- roll_speed - FloatLE - Velocidade da esteira de roletes (0.0 a 0.3).
- angle - FloatLE - "Posição angular da mesa rotativa (0.0 para reto, 90.0 para desvio)."
- sensor_status - Int / Array - Retorna 1 (caixa detectada) ou 0 (livre).
- led_color - Byte - "Cor do PickLight (0 = Vermelho, 1 = Verde, 2 = Amarelo)."