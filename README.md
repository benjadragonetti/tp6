# tp6
#include <math.h>
#include <stdio.h>
#define Pi 3.14
int opc;
float calcularAreaRectangulo(int alt, int longitud){
    float area1;
    area1 = (float) alt * longitud;
    
    return area1;
}
float calcularPerimetroRectangulo(int alt, int longitud){
    float perim1;
    perim1 = 2 * (longitud + alt);
    
    return perim1;
}
float calcularDiagonalRectangulo(int alt, int longitud){
    float diag;
    
    diag = sqrt( pow(alt, 2) + pow(longitud, 2));

    return diag;
    
}
float calcularAreaCirculo(int rad){
   float area2;

   area2 = Pi * pow(rad, 2);
   
   return area2;
}
float calcularPerimetroCirculo(int rad){
 float perim2;

   
   perim2 = 2 * Pi * rad;
   
   
   return perim2;
}
float imprimirResultados(float area1, float perim1, float diag, float area2, float perim2, int opc){

   if(opc==1){
   printf("En el rectangulo\n");
   
   printf("El area es: %.2f \n", area1);
  
   printf("El perimetro es: %.2f \n", perim1);
  
   printf("La diagonal es: %.2f \n", diag);
   }
   
   if(opc==2){
   printf("En el circulo\n");
   
   printf("El area es: %.2f \n", area2);
   
   printf("El perimetro es: %.2f \n", perim2);
   }
}

int main()
{
    int alt, longitud, rad;
    float area1, perim1, diag, area2, perim2, resultado1, resultado2;
    printf("1 - Area, perimetro y diagonal de rectangulo \n");
    printf("2 - Area y perimetro de circulo \n");
    printf("Ingrese la opcion que desea ejecutar:");
    scanf("%d", &opc);
    
    switch(opc)
    {
        case 1:
           printf("Elegiste el area, perimetro y diagonal del rectangulo\n");
           
           printf("Introduce la altura del rectangulo:");
           scanf("%d" ,&alt);
           printf("Introduce la longitud del rectangulo:");
           scanf("%d", &longitud);
           
           area1=calcularAreaRectangulo(alt,longitud);
           
           perim1=calcularPerimetroRectangulo(alt,longitud);
           
           diag=calcularDiagonalRectangulo(alt,longitud);
           
           resultado1 = imprimirResultados(area1,perim1,diag,area2,perim2,opc);
           
           break;
           
            case 2:
           printf("Elegiste el area y perimetro del rectangulo\n");
           
           printf("Introduce el radio del circulo:");
           scanf("%d" ,&rad);
           
           area2 = calcularAreaCirculo(rad);
           
           perim2 = calcularPerimetroCirculo(rad);
           
           resultado2 = imprimirResultados(area1,perim1,diag,area2,perim2,opc);
           
           break;
            
         

    }
    return 0;
} 
