# Piano Eletrônico de 7 Notas com Arduino 💗🎶✨

Este projeto apresenta um piano eletrônico simplificado desenvolvido no **Tinkercad**, utilizando uma placa Arduino Uno para processar entradas de botões e gerar sons através de um buzzer.

## 🚀 Visão Geral
O sistema mapeia 7 botões (push-buttons) para a escala musical básica. Ao pressionar cada botão, o Arduino identifica o sinal de entrada e aciona um Buzzer Piezo com uma frequência específica, simulando as notas musicais.

## 🛠️ Hardware e Componentes
* **1x Arduino Uno R3**: O cérebro do projeto.
* **1x Piezo Buzzer**: Responsável pela saída sonora.
* **7x Botões (Push-buttons)**: Utilizados para as teclas do piano.
* **7x Resistores de 10kΩ**: Configurados em modo **Pull-Down** para evitar leituras flutuantes.
* **1x Protoboard**: Para a montagem do circuito.
* **Jumpers**: Fios de conexão coloridos para organização.

## 📋 Mapeamento de Notas e Pinos
As conexões foram realizadas conforme a tabela abaixo:

| Nota | Pino Digital | Frequência (Hz) |
| :--- | :---: | :---: |
| DO  | 2 | 200 |
| RE  | 3 | 220 |
| MI  | 4 | 250 |
| FA  | 5 | 260 |
| SOL | 6 | 290 |
| LA  | 7 | 330 |
| SI  | 8 | 370 |
| **Buzzer** | **11** | - |

## 💻 Lógica do Software
O código foi desenvolvido de forma modular e intuitiva:
1.  **Declaração**: Variáveis amigáveis são atribuídas aos pinos digitais para facilitar a leitura.
2.  **Setup**: Define os pinos dos botões como entradas (`INPUT`) e o buzzer como saída (`OUTPUT`).
3.  **Loop**:
    * O Arduino lê constantemente o estado dos pinos (`digitalRead`).
    * Se um botão for pressionado (`bot == 1`), a função `tone()` é executada.
    * `tone(Buzzer, frequência, duração)` gera o som correspondente por 100ms.

## ⚙️ Montagem do Circuito
* **Alimentação**: O barramento positivo da protoboard é ligado aos 5V do Arduino e o negativo ao GND.
* **Entradas**: Cada botão está ligado entre os 5V e um pino digital, com um resistor de 10kΩ ligando o pino ao GND (garantindo nível lógico 0 quando em repouso).
* **Saída**: O terminal positivo do Buzzer está conectado ao pino digital 11.

---
**Programadora:** Sarah Mendonça  💗🪻🦋
*Uhuuu. Já podemos colocar em prática!* 🎹✨
