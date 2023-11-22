# Global Solution Edge

Este projeto foi desenvolvido em parceria com a HapVida, com o objetivo de criar uma solução inovadora e acessível para monitorar indicadores vitais de saúde, como a temperatura corporal e a frequência cardíaca. Utilizando tecnologias IoT (Internet das Coisas), o sistema coleta dados em tempo real e os envia para uma plataforma de monitoramento, permitindo que os usuários ou profissionais de saúde acompanhem essas métricas de forma contínua. Este sistema tem o potencial de impactar significativamente o bem-estar dos indivíduos, permitindo uma resposta rápida a possíveis condições adversas de saúde e promovendo um estilo de vida saudável.

## Impacto na Saúde
A monitorização constante dos sinais vitais pode ser crucial para pacientes com condições crônicas, idosos, ou aqueles em recuperação pós-operatória. O acesso a dados em tempo real e a análise contínua permitem:
Detecção precoce de padrões anormais, potencializando intervenções rápidas.
Melhor compreensão da própria saúde pelos usuários, incentivando a autogestão e o cuidado preventivo.
Dados históricos valiosos durante as consultas médicas, contribuindo para diagnósticos mais precisos e tratamentos personalizados.
## Componentes Técnicos
## Hardware
ESP32: Microcontrolador com Wi-Fi integrado, usado como a unidade central de processamento e comunicação do sistema.
Sensor de Temperatura (DHT22): Mede a temperatura ambiente, que pode ser utilizada como referência para a temperatura corporal em simulações.
Potenciômetro: Simula a variação dos batimentos cardíacos. Ajustando o potenciômetro, altera-se a "frequência cardíaca" que o sistema irá monitorar.
LED Vermelho: Fornece feedback visual do "batimento cardíaco". Piscará em um ritmo proporcional à frequência cardíaca simulada.
## Software
Arduino IDE: Para programar o ESP32.
Node-RED: Plataforma de fluxo que executa no Node.js, usada para construir o backend que processa e exibe os dados.
MQTT Protocol: Protocolo leve de mensagens para comunicação M2M (Machine to Machine), utilizado para transmitir dados entre o ESP32 e o Node-RED.
## Integração e Fluxo de Dados
Coleta de Dados: O ESP32 lê a temperatura do sensor DHT22 e os "batimentos cardíacos" do potenciômetro.
Processamento de Dados: O ESP32 processa os dados e os envia para o broker MQTT HiveMQ.
Transmissão de Dados: Os dados são publicados em tópicos MQTT específicos.
Node-RED: Subscreve aos tópicos MQTT e utiliza funções para processar e exibir os dados em um dashboard ou armazenar para análises futuras.
## Configuração e Uso
Para implementar o projeto, siga estes passos:

Montagem do Circuito: Conecte o DHT22, o potenciômetro e o LED ao ESP32 conforme a documentação técnica.
Programação do ESP32: Utilize a Arduino IDE para carregar o código fornecido ao microcontrolador.
Configuração do Node-RED: Importe o fluxo fornecido e ajuste as funções conforme necessário.
Monitoramento: Acesse o dashboard do Node-RED para visualizar os dados em tempo real.

## Link para o Vídeo
https://youtu.be/8oxiVT8Uddk?si=IoMSMJ7kJXiK_sU2

## Link para a simulação do projeto no Wokwi
https://wokwi.com/projects/381965574176880641

## RM98650 - JOÃO PEDRO CRUZ
## RM551169 - TIAGO PAULINO

