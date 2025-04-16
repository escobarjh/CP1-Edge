Projeto de Monitoramento de Luminosidade com LEDs e Buzzer (Arduino)

Este projeto utiliza um Arduino para monitorar a luminosidade de um ambiente. Ele usa um sensor LDR (Light Dependent Resistor) para medir a intensidade da luz e, dependendo do valor lido, aciona LEDs de diferentes cores e um buzzer para indicar se a luminosidade está dentro dos níveis ideais, em alerta ou crítica. O sistema tem três estados de luminosidade: ideal, alerta e crítico.

Componentes Utilizados:

Arduino Uno (ou qualquer placa compatível)
1 Sensor LDR (resistor dependente de luz)
3 LEDs: Verde, Amarelo e Vermelho
1 Buzzer
Resistor de 10kΩ (para o sensor LDR)
Fios de conexão
Protoboard (opcional)

Como Funciona o Sistema :

O sensor LDR mede a intensidade da luz no ambiente. O valor que ele retorna varia de 0 a 1023, sendo que valores baixos significam que há mais luz e valores altos indicam que a luz está mais fraca. Com base nesses valores, o sistema aciona os LEDs e o buzzer de acordo com as seguintes condições:
Condição Ideal de Luminosidade (0 a 200):
O LED verde acende, indicando que a luz está em níveis ideais.
Os LEDs amarelo e vermelho permanecem apagados.
O buzzer fica desativado.
Alerta Moderado de Luminosidade (201 a 550):
O LED amarelo acende, indicando um alerta moderado de luminosidade.
Os LEDs verde e vermelho ficam apagados.
O buzzer permanece desativado.
Condição Crítica de Luminosidade (acima de 550):
O LED vermelho acende, indicando que a luminosidade está em níveis críticos.
O buzzer começa a emitir um som contínuo com uma frequência de 250 Hz por 200ms, seguido de uma pausa de 300ms. Esse ciclo de som se repete enquanto a condição crítica persistir.
Os LEDs verde e amarelo permanecem apagados.

Como Montar o Circuito 

Aqui está o esquema de como conectar os componentes:

Sensor LDR: Conecte o LDR entre o pino A0 do Arduino e o GND. Coloque um resistor de 10kΩ entre o pino A0 e o 5V para formar um divisor de tensão.
LED Verde: Conecte o ânodo do LED ao pino digital 7 e o cátodo ao GND, com um resistor de 220Ω em série.
LED Amarelo: Conecte o ânodo ao pino digital 13 e o cátodo ao GND, também com um resistor de 220Ω.
LED Vermelho: Conecte o ânodo ao pino digital 8 e o cátodo ao GND, com um resistor de 220Ω em série.
Buzzer: Conecte o pino positivo do buzzer ao pino digital 12 do Arduino e o pino negativo ao GND.

Como Usar o Sistema :

Prepare o hardware: Conecte todos os componentes conforme o esquema de conexões descrito acima.
Carregue o código: Abra o Arduino IDE, cole o código do projeto e carregue-o no seu Arduino.
Monitore as saídas: Abra o Monitor Serial para acompanhar os valores de leitura do sensor LDR e veja como os LEDs e o buzzer reagem conforme a intensidade da luz.

Considerações Finais : 

Este projeto é ótimo para monitoramento de luz em ambientes internos, e pode ser adaptado para várias situações, como controle automático de iluminação, monitoramento de plantas (jardinagem) ou até mesmo para sistemas de energia solar. É uma solução simples e prática para entender como medir e reagir a condições de luminosidade com o Arduino.
