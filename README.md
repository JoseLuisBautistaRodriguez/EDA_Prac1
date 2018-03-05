#include <stdio.h>
#include<stdlib.h>
  
int main(){
   
	int numero, numero2, numero3, numero4, x, cociente[1001], factorPrimo[1000];  
	int fact = 2, i = 0;
	   
    int est1=1;
    
     puts("			EL PROGRAMA DE LOS FACTORES PRIMOS\n\n");
     	printf("Ingrese un numero entero: "); 
	 		scanf("%d", &numero);
			fflush(stdin);
     
  	 if(numero<1)printf("\nDato no valido.");
     else if (numero==1)printf("\n     ADVERTENCIA! \n\t No tiene factores primos.");
     else {
          numero4=numero;
          while(numero>1){
                 if(numero%fact==0){
                        numero2=numero; numero/=fact; numero3=numero2/fact;
                        	if(est1){
                             	factorPrimo[0]=fact; 
								 	cociente[0]=numero3; 
								 		est1=0;
                        	}
                        	else {
                            	i++; factorPrimo[i]=fact;
								 	 cociente[i]=numero3;
                        	}
                  }
        	else
        		fact++;
           }
           
		   printf("\nNumero ingresado: %d\n",numero4);
           printf("\nFactores primos: %d\n",factorPrimo[0]);
           
		   for(x=1;x<=i;x++)
                  printf("\t%d",factorPrimo[x]);
           printf("\nCocientes de factorizacion: %d\n",cociente[0]);
            for(x=1;x<=i;x++)
                  printf("\t%d",cociente[x]);
       }
       return 0;
       
   }
