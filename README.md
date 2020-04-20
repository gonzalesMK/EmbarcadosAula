# Projeto Pick and Place

## Descrição
O seguinte projeto está sendo desenvolvido para a discplina de Sistemas embarcados do curso de engenharia mecatrônica. O objetivo do projeto é desenvolver um sistema de pick and place de um grau de liberdade que seja capaz de detectar a presênça de uma carga, realizar a sua movimentação, agarrar o objeto e leva-lo para outro lugar. Os materiais utilizados na realização desse projeto serão de fácil acesso e custo reduzido.

## Materiais:
- Beagle Black Bone.
- Controlador EPOS2.   
- Motor Maxon com encoder.
- Sensor ultrasônico HC-SR04.
- Garra.
- Servo motor.

## Requisitos:

- O projeto deve ser capaz de posicionar o motor de tal forma que o posicionamento final da carga seja precisa. Ao utilizarmos o controlador EPOS teremos fácil acesso aos valores do encoder do motor e dos valores da velocidade do motor, dessa forma o controle da posição final será de fácil implementação.

- O projeto deve ser capaz de detectar a presênça da carga para movimentação. Para isso vamos utilizar o sensor ultrasom HC-SR04, detectando a presênça a carga medindo a distância detectada. Para realizar a leitura desse sensor é necessário somente realizar a leitura de dois pinos e fazer uma contagem de tempo no software.

- O microcontrolador utilizado deve ser capaz de realizar a leitura de portar digitais, comunicar com o controlador de motores e aceitar a utilização de diversas bibliotecas de programação necessárias, como a do controlador EPOS fornecido pela própria Maxon. A Beagle Black Bone atende a todos esses requisitos.

- O projeto deve ser capaz de segurar uma carga leve e não derruba-la enquanto ele realiza o seu movimento. O acionamento da garra sera feito por meio de um servo motor. 

- A movimentação do pick and place será feito atráves da interação de um mecanismo com a rotação do motor. A ideia e utilizar o controlador para movimentar o motor a quantidade certa de forma a criar um movimento pausado e com precisão. Um exemplo da mecânica do projeto pode ser visto no link a seguir: https://www.youtube.com/watch?v=Ghc_rZ49Q8A&feature=youtu.be.

