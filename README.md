# NerdDoor_FingerPrint
Tutorial de como o sensor de dedo funciona 
Neste github vai estar decumentado tudo sobre o sensor e o código.

O sensor é o SFM-V1.7. (git do sensor:https://github.com/Matrixchung/SFM-V1.7).

Como microcontrolador é usado um ESP-8266.

# Montagem do circuito

Na decumentação do sensor temos esta imagem
![image](https://github.com/quevinlm27/NerdDoor_FingerPrint/assets/173367448/0dfdd413-a5ec-4d2e-a1d8-a9833e2c85bc)

O fio azul serve para gerar uma interrupção se o sensor for tocado. (Nunca consegui por a funcionar e funciona sem estar ligado a nada).

Os fios amarelo e preto são TX e RX mas dá mais jeito ligar aos pinos GPIO que não são da UART. Usar estes pinos faz com que se tiverem ligados não dá para mandar código.

De resto é só ligar como diz na figura.

# MQTT

A porta funciona através de um conceito chamado MQTT. Recomendo ver um ou dois videos sobre o que é para se tornarem familiarizados.
Para se conectarem precisam de estar ligados a internet do NerD.

A lógica por trás do fingerprint é bastante simples. Usando as funções da biblioteca do sensor vemos se o dedo está registado. Se estiver manda uma mensagem para o MQTT que por si abre a porta.









