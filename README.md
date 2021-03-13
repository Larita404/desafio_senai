# desafio_senai

Para executar o desafio inicialmente alterei a distância mínima do obstáculo para 100 metros.
Apenas esta alteração já foi o suficiente para que o robo chegasse no tempo estipulado ao ponto de chegada.

------------------------------------------------------------------
// minimal distance, in meters, for an obstacle to be considered
#define MIN_DISTANCE 100.0
-------------------------------------------------------------------

Para que o mesmo parasse ao chegar, adicionei um GPS e um receptor. verifiquei em quais coordenadas do quadrante se encontravam o poste de luz e a placa de stop, imprimindo as coordenadas do robô. Então adicionei uma clausula 'if' dentro do while, para que ao atingir estas coordenadas a velocidade das rodas fosse para 0.

-------------------------------------------------
 if (gps_values[0] <-5.4 && gps_values[2] >3){  
  wb_motor_set_velocity(left_wheel, 0.0);
  wb_motor_set_velocity(right_wheel, 0.0);
        break;
       } 
------------------------------------------------
