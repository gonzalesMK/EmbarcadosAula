# Projeto Pick and Place

## Descrição
O seguinte projeto está sendo desenvolvido para a discplina de Sistemas embarcados do curso de engenharia mecatrônica. O objetivo do projeto é desenvolver um sistema de pick and place de um grau de liberdade que seja capaz de detectar a presênça de uma carga, realizar a sua movimentação, agarrar o objeto e leva-lo para outro lugar. Esse projeto está sendo desenvolvido para a discplina de Sistemas Embarcados (SEM0544, 1o semestre de 2020) do Curso de Engenharia Mecatrônica EESC-USP.

![Mecânica imaginada até o momento](https://i.imgur.com/e1GqOqN.png)

## Integrantes:


## Materiais:
- Beagle Black Bone.
- Controlador EPOS2.   
- Motor Maxon com encoder.
- Sensor ultrasônico HC-SR04.
- Garra.
- Servo motor.

## Requisitos:

- O projeto deve ser capaz de posicionar o motor de tal forma que o posicionamento final da carga seja precisa em relação às posições. Também é necessário que o movimento do pick and place seja suave e que já ocorra overshhot grande das posições. 

- O projeto deve ser capaz de detectar a presença da carga para movimentação. 

- O projeto deve ser capaz de segurar uma carga leve e não derruba-la 90% das vezes enquanto ele realiza o seu movimento do ponto final ao inicial.

- A movimentação do pick and place será feito atráves da interação de um mecanismo com a rotação do motor. O tempo de realização do ciclo de pegar e soltar a carga deve ser de aproximadamente 5 segundos. 

## Possíveis Solucões para os requisitos:

- Ao utilizarmos o controlador EPOS teremos fácil acesso aos valores do encoder do motor e dos valores da velocidade do motor, dessa forma o controle da posição final será de fácil implementação. Será utilizado a biblioteca própria da EPOS, que pode ser baixada, instalada e ter suas funções estudadas no seguinte PDF: https://www.maxongroup.com/medias/sys_master/8823917281310.pdf. Um código de exemplo do acionamento dos motores pode ser visto neste repositório.

- Para isso vamos utilizar o sensor ultrasom HC-SR04, detectando a presênça a carga medindo a distância detectada. Para realizar a leitura desse sensor é necessário somente realizar a leitura de dois pinos e fazer uma contagem de tempo no software. Para realizar a leitura dos pinos, atualmente se cogita utilizar esse repositório: https://github.com/mkaczanowski/BeagleBoneBlack-GPIO

- O acionamento da garra sera feito por meio de um servo motor. Talvez seja necessário colocar fita grudante na ponta para garantir aderência.

- A ideia é utilizar o controlador para movimentar o motor a quantidade certa de forma a criar um movimento pausado e com precisão. Um exemplo da mecânica do projeto pode ser visto no link a seguir: https://www.youtube.com/watch?v=Ghc_rZ49Q8A&feature=youtu.be.


