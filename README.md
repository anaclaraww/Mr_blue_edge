## Projeto Arduino para Detecção de Garrafas Plásticas no Oceano 🌊

**Introdução**

Este projeto Arduino visa integrar um sistema de detecção de garrafas plásticas em um drone, utilizando sensores e futuramente enviar as informações coletadas para um site web. O sistema consiste em:

* **Sensores:**
    * DHT11: Medição de temperatura e umidade
    * LDR: Detecção de luminosidade (escuro/claro)
    * GPS (simulado): Obtenção de coordenadas geográficas
* **Atuadores:**
    * LEDs: Sinais visuais para indicar o status do sistema
* **Comunicação:**
    * LCD IC2: Componene visual com circuito integrado.
    * Envio de dados para python (intenção)

**Componentes Utilizados:**

* Módulo Arduino
* Sensor DHT11
* Sensor LDR
* LCD ic2
* LEDs
* Módulo GPS simulado (adaptado da versão de Anderson Costa)

**Funcionamento do Sistema:**

1. **Leitura dos Sensores:**
    * O sensor DHT11 coleta dados de temperatura e umidade.
    * O sensor LDR detecta a luminosidade do ambiente.
    * O módulo GPS simulado fornece as coordenadas geográficas do drone.
2. **Processamento dos Dados:**
    * Os dados dos sensores são processados pelo Arduino.
    * A detecção de garrafas plásticas é realizada com base em algoritmos específicos.
3. **Acionamento dos Atuadores:**
    * LEDs acendem para indicar o status do sistema (por exemplo, ligado, buscando garrafas, garrafas detectadas).
4. **Comunicação com o Site Web:**
    * Os dados coletados e processados são enviados para um site web via Wi-Fi ou rede celular (opcional).
    * O site web exibe as informações em tempo real e permite o monitoramento do sistema.
  
**Bibliotecas Necessárias:**

     <DHT.h>; 
     <LiquidCrystal_I2C.h>;
     <SoftwareSerial.h>;
    
**Resumo das Bibliotecas:**
| Biblioteca | Função |
|---|---|
| DHT.h | Interagir com o sensor DHT11 (temperatura e umidade) |
| LiquidCrystal_I2C.h | Controlar display LCD via I2C |
| NMEA.h | Interpretar dados NMEA do simulador GPS |
| SoftwareSerial.h | Simular porta serial para comunicação com simulador GPS |

**Estrutura do projeto**


```plaintext
Mr_blue_edge/
├── README.md                  
├── simulador_gs/                   
│   ├── DHT.h                 # Biblioteca DHT para sensor DHT11
│   ├── LiquidCrystal_I2C.h     # Biblioteca LiquidCrystal_I2C para display LCD 
│   ├── NMEA.h                 # Biblioteca NMEA para simulador GPS (utilizada para  o simulador)
│   ├── SoftwareSerial.h        # Biblioteca SoftwareSerial para comunicação serial simulada
│   └── sketch.ino             # Arquivo com o código Arduino com simulador GPS, DHT11 e LDR(sem leds)
├── simulador_gs/                   
│   ├── sketch.ino             # Arquivo com o código Arduino com demostração das led e LDR.
```

> [!WARNING]
> projeto possui duas versões pois o simulador de GPS interfere no acendimento das Leds, porém é uma condição que não aconteceria em equipamentos reias.

**Simulação simulador_gs/**


<img src="https://github.com/anaclaraww/Mr_blue_edge/blob/main/simulador_gs.png" alt="Texto Alternativo">

**Simulação simulador_led_gs/**


<img src="https://github.com/anaclaraww/Mr_blue_edge/blob/main/simulador_led.png" alt="Texto Alternativo">

**Benefícios do Projeto:**

* **Monitoramento Ambiental:** Coleta de dados de temperatura, umidade e luminosidade do ambiente marinho.
* **Detecção de Poluição:** Identificação e localização de garrafas plásticas flutuando no oceano.
* **Conservação Marinha:** Auxílio na preservação do meio ambiente através da coleta de dados sobre a poluição por plástico.
* **Pesquisa Científica:** Fornecimento de dados valiosos para pesquisas sobre a poluição marinha e o impacto do plástico nos oceanos.

**Próximos Passos:**

* **Desenvolvimento do Algoritmo de Detecção:** Aprimorar o algoritmo para identificar garrafas plásticas com maior precisão.
* **Integração com o Módulo GPS Real:** Substituir o módulo GPS simulado por um módulo real para obter dados geográficos precisos.
* **Implementação da Comunicação com Site Web:** Desenvolver a interface web para receber e exibir os dados coletados pelo sistema.
* **Testes e Validação:** Realizar testes extensivos para garantir o funcionamento correto do sistema em diferentes condições.
* **Implementação em Drones Reais:** Adaptar o sistema para integração em drones reais e realizar testes em campo.


###Desenvolvido por: Ana Clara Melo (RM559021)
