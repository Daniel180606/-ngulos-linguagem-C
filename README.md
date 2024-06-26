# angulos-linguagem-C
Programa que recebe a medida de um ângulo e mostre o quadrante em que se localiza
#include <stdio.h>

int main(void) {
 int angulo,voltas,quadrante,faltavolta;//declaração das variaveis
  scanf("%d",&angulo);//Leia angulo 
  if ( angulo % 90 == 0 || angulo % 180 == 0 || angulo % 270 == 0|| angulo % 360 == 0){ // se o resto da divisão por 90, 180, 270 e 360 for 0 
      printf("Este angulo se encontra em um dos eixos\n");//imprima a expressão "Este angulo se encontra em um dos eixos"
  }
  if (angulo >=0 && angulo <=90 || angulo < -270 && angulo >= -360){//se o angulo for maior ou igual a zero e menor ou igual a 90 ou angulo for menor que -270 e angulo for maior ou igual a -360
    printf ("primeiro quadrante\n");// imprima a expressão "primeiro quadrante"
  }
  if(angulo > 90 && angulo <= 180 || angulo < -180 && angulo >= -270 ){//se o angulo for maior do que 90 e menor ou igual a 180 ou angulo for menor que -180 e angulo for maior ou igual a -270
     printf ("segundo quadrante\n");// imprima a expressão "segundo quadrante"
    }
  if(angulo > 180 && angulo <= 270 || angulo < -90 && angulo >= -180){//se o angulo for maior do que 180 e menor ou igual a 270 ou angulo for menor que -90 e angulo for maior ou igual a -180
   printf ("terceiro quadrante\n"); // imprima a expressão "terceiro quadrante"
  }
  if(angulo > 270 && angulo <= 360 || angulo <=0 && angulo >=-90){//se o angulo for maior do que 270 e menor ou igual a 360 ou angulo for menor ou igual a 0 e angulo for maior ou igual a -90
   printf ("quarto quadrante\n"); // imprima a expressão "quarto quadrante"
  }
  if (angulo + 720 <=0 && angulo + 720 >=-90){ // se angulo + 720 for menor ou igual a 0 e angulo + 720 for maior ou igual a -90
    printf("quarto quadrante\n");// imprima a expressão "quarto quadrante"
  }
  if (angulo < -720){ // se angulo for menor que -720
    printf ("2 volta(s) sentido horario\n");
  }
  if (angulo < -720){ // se angulo for menor que -720
    faltavolta = 1080 + angulo;// faltavolta = 1080 + angulo
    printf ("Falta(m) %d graus (sentido horario) para completar 3 volta(s)", faltavolta);// imprima a expressão "Falta(m) %d graus (sentido horario) para completar 3 volta(s)" e imprima o valor de faltavolta
  }
  if (angulo - 360 <90 && angulo - 360 == 0){// se angulo - 360 for menor que 90 e angulo -360 for igual a 0
    printf ("primeiro quadrante\n");// imprima a expressão "primeiro quadrante"
  }
  if (angulo - 360 <=180 && angulo - 360 > 90){// se angulo - 360 for menor ou igual a 180 e angulo -360 for maior que 90
    printf ("segundo quadrante\n");// imprima a expressão "segundo quadrante"
  }
  if (angulo - 360 <=270 && angulo - 360 > 181){// se angulo - 360 for menor ou igual a 270 e angulo -360 for maior que 181
    printf ("terceiro quadrante\n");// imprima a expressão "terceiro quadrante"
  }
  if (angulo - 360 <=360 && angulo - 360 > 271){// se angulo - 360 for menor ou igual a 360 e angulo -360 for maior que 271
    printf ("quarto quadrante\n");// imprima a expressão "quarto quadrante"
  }

  if (angulo >= 0 && angulo <= 360){// se angulo for maior ou igual a zero e angulo for menor ou igual a 360
    printf("0 volta(s) sentido antihorario\n");// imprima a expressão 0 volta(s) sentido antihorario"
  }
  if (angulo <360 && angulo >0) {// se angulo for menor que 360 e angulo for maior que 0
    faltavolta= 360 - angulo;// faltavolta = 360 - angulo
    printf("Falta(m) %d graus (sentido antihorario) para completar 1 volta(s)\n", faltavolta);// imprima a expressão "Falta(m) %d graus (sentido antihorario) para completar 1 volta(s)" e imprima o valor de faltavolta
  }
  if (angulo > 360){// se angulo for maior que 360
    faltavolta= 720-angulo;// faltavolta = 720 - angulo
    printf("1 volta(s) sentido antihorario\n" "Falta(m) %d graus (sentido antihorario) para completar 2 volta(s)\n", faltavolta);// imprima a expressão "1 volta(s) sentido antihorario" e "Falta(m) %d graus (sentido antihorario) para completar 2 volta(s), e  imprima o valor de faltavolta
  }
  if (angulo < 0 && angulo > -130){// se angulo for menor que 0 e maior que -130
    printf ("0 volta (s) sentido horario\n");// imprima a expressão "0 volta (s) sentido horario"
  }
  if (angulo <0 && angulo >=-360){// se angulo for menor que 0 e maior ou igual a -360
    faltavolta= 360 + angulo;// faltavolta = 360 + angulo
    printf("Falta(m) %d graus (sentido horario) para completar 1 volta(s)\n", faltavolta);// imprima a expressão "Falta(m) %d graus (sentido horario) para completar 1 volta(s)" e imprima o valor de faltavolta
  }

  return 0;
}
