# Projeto Pick and Place

## Descrição
O objetivo do projeto é desenvolver um sistema pick and place de um grau de liberdade que seja capaz de detectar a presença de uma carga em um local e move-lo para outro lugar específico dentro de alguns requisitos de tempo e performance. Esse projeto está sendo desenvolvido para a discplina de Sistemas Embarcados (SEM0544, 1o semestre de 2020) do Curso de Engenharia Mecatrônica EESC-USP.

![Mecânica imaginada até o momento](https://i.imgur.com/e1GqOqN.png)

## Integrantes:
- Lucca Neves Maitan (9805376)
- Matheus Passaura Marcolino (9805171)

## Materiais:
- Beagle Black Bone.
- Controlador EPOS2.   
- Motor Maxon com encoder.
- Sensor ultrasônico HC-SR04.
- Garra.
- Servo motor.

## Requisitos:

- O projeto deve ser capaz de mover o motor de tal forma que o posicionamento final da carga seja precisa em relação às posições. Também é necessário que o movimento do pick and place seja suave e que ocorra overshoot pequeno ou nulo durante o movimento entre as posições. 

- O projeto deve ser capaz de detectar a presença da carga para movimentação. 

- O projeto deve ser capaz de segurar uma carga leve e não derruba-la 90% das vezes enquanto ele realiza o seu movimento do ponto final ao inicial.

- A estrutura mecânica deve ser firme e permitir um movimento suave nas articulações.

- O sistema deve conseguir pegar um objeto com dimensões A x B x C mm e soltá-lo para uma distância de D mm a partir do ponto de coleta. As dimensões do sistema 4 barras e do projeto mecânico da estrutura será calculada a partir dessas dimensões especificadas.

- A movimentação do pick and place será feito atráves da interação de um mecanismo com a rotação do motor. O tempo de realização do ciclo de pegar e soltar a carga deve ser de aproximadamente 5 segundos. 

## Possíveis Solucões para os requisitos:

- Ao utilizarmos o controlador EPOS teremos fácil acesso aos valores do encoder do motor e dos valores da velocidade do motor, dessa forma é facilitada a implementação do controle de posição final. Será utilizado a biblioteca própria da EPOS, que pode ser baixada, instalada e ter suas funções estudadas no seguinte PDF: https://www.maxongroup.com/medias/sys_master/8823917281310.pdf. Um código de exemplo do acionamento dos motores pode ser visto neste repositório.

- Para isso vamos utilizar o sensor ultrasom HC-SR04, detectando a presença da carga ao medir a distância detectada. Para realizar a leitura desse sensor é necessário somente realizar a leitura de dois pinos e fazer uma contagem de tempo no software. Para realizar a leitura dos pinos, atualmente se cogita utilizar esse repositório: https://github.com/mkaczanowski/BeagleBoneBlack-GPIO

- O acionamento da garra será feito por meio de um servo motor. Talvez seja necessário colocar algum material na área de contato da garra com o objeto para maximizar a aderência, como algum material emborrachado por exemplo.

- A ideia é utilizar o controlador para movimentar o motor a quantidade certa de forma a criar um movimento pausado e com precisão. Um exemplo da mecânica do projeto pode ser visto no link a seguir: https://www.youtube.com/watch?v=Ghc_rZ49Q8A&feature=youtu.be.

- Planeja-se construir a estrutura e o mecanismo a partir de barras vazadas de perfil quadrado de aproximandamente E x E mm, por conta de sua alta resistência em conjunto com o baixo peso. As articulações poderão ser feitas a partir de parafuso e porca através de furos nas barras, procedimento já realizado com sucesso em projetos anteriores.

- Como o objeto movido será em formato de caixa, poderá ser projetada uma garra com movimento paralelo, maximizando a área de contato e por consequência o atrito. A garra poderá ser feita por manufatura aditiva, facilitando a fabricação e o encaixe das partes e do atuador.


