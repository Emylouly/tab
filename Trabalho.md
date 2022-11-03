//1. Crie um programa em C para armazenar 100 números sorteados aleatoriamente em um vetor e, em seguida, criar dois vetores: Um com os números ímpares e outro com os números pares. Imprimir os vetores resultantes.

#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale(LC_ALL, "Portuguese");
	srand(time(NULL));
	
	int a[100], pares[100], impares[100], x, y;
	
	printf("Vetores sorteados: \n\n");
	for(y=0; y<100; y++){
		
		a[y]=rand()%1000;
		
		printf("%d ", a[y]);	
		
	}
	
			
	printf("\n\nVetores pares:\n\n");
	for(y=0; y<100; y++){
		
		pares[y]=a[y];

			if(pares[y]%2==0){
		 	printf("%d ", pares[y]);
		 
		}		
	}
	
	
	printf("\n\nVetores impares:\n\n");
	for(y=0; y<100; y++){
		
		impares[y]=a[y];

			if(impares[y]%2!=0){
			printf("%d ", impares[y]);
		 
		}		
	}
}


//2. Fazer um programa para preencher com números aleatórios entre 0 e 1000, um vetor com 300 posições. Em seguida, mostrar a soma dos valores sorteados, a media dos numeros sorteados e a posição do vetor onde se encontra o maior e o menor numero. 

#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale(LC_ALL, "Portuguese");
	srand(time(NULL));

	int a[300], soma=0, y, media, maior=0, menor=1000, posicaomaior, posicaomenor;
	
	printf("Vetores sorteados: \n\n");
	for(y=0; y<300; y++){
		
		a[y]=rand()%1000;
		
		printf("%d ", a[y]);
		
		soma = soma + a[y];
			
	}
	

	for(y=0; y<300; y++){
		if(a[y]>maior){
			
			maior=a[y];
			posicaomaior=y;
			
		}
		
			else if(a[y]<menor){
			
			menor=a[y];
			posicaomenor=y;
		}
}	
	
	media=soma/300;
	
	printf("\n\nSoma: %d \nMedia: %d \nMaior: %d e está na posição %d \nMenor: %d e está na posição %d", soma, media, maior, posicaomaior, menor, posicaomenor);
}



//3. Faça um programa para ler, ou preencher com números aleatórios, uma matriz 3 x 3, e crie um vetor com os números pares existentes na matriz. Depois, imprimir a matriz e o vetor.


#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale(LC_ALL, "Portuguese");
	srand(time(NULL));

	int a[3][3], pares[9], y, x, z, p=0, j, n, k=0;
	
	printf("Escolha uma das opções a baixo: \n\n1 - Caso queira preencher a matriz digite 1. \n2 - Caso queira que a matriz seja preenciada com números aleatórios digite 2. \n\nSelecione a sua opção: ");
	scanf("%d", &j);
	
	switch(j){
		
	case 1:
		
	k++; //variavel de controle para a opção valida
		
		printf("\n\nDigite os números para preencher a matriz: \n\n");	
		for(y=0; y<3; y++){	
			for(x=0; x<3; x++){
			
			printf("a[%d][%d] = ", y, x);
			scanf("%d", &n);
			
			a[y][x]=n;
		}
			
	}
		
		printf("\n\nMatriz digitada: \n\n");			
		for(y=0; y<3; y++){
			for(x=0; x<3; x++){
			
			printf("%2d ", a[y][x]);
		}
			
		printf("\n");	
	}
		break;

		
	case 2:
	
	k++; //variavel de controle para a opção valida
	
	printf("\n\nMatriz sorteada: \n\n");
	for(y=0; y<3; y++){
		for(x=0; x<3; x++){
		
		a[y][x]=rand()%30;	
			printf("%2d ", a[y][x]);
		
		}
		
		printf("\n");		
	}
		break;
	

	default:
		printf("\n\n*Opção invalida!!!*\n\n*Tente Novamente!!!*");
	
}

	if(k!=0){
	
	printf("\n\nNúmeros pares da matriz: ");
	
		for(y=0; y<3; y++){
		
			for(x=0; x<3; x++){
			
			if(a[y][x]%2==0){
				
			p++;
			
			pares[p]=a[y][x];
			
			printf("%d ", pares[p]);
			
			}			
		}
	}
}
}


//4. Faça um programa para ler, ou preencher com números aleatórios, uma matriz 6 x 6, e imprima a quantidade de números impares e todos os números impares existentes na matriz.


#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale(LC_ALL, "Portuguese");
	srand(time(NULL));

	int a[6][6], impares[36], y, x, z, soma=0, j, n, k=0;
	
	printf("Escolha uma das opções a baixo: \n\n1 - Caso queira preencher a matriz digite 1. \n2 - Caso queira que a matriz seja preenciada com números aleatórios digite 2. \n\nSelecione a sua opção: ");
	scanf("%d", &j);
	
	switch(j){
		
	case 1:
	k++/ //variavel de controle para indicar a opção valida	
	
		printf("\n\nDigite os números para preencher a matriz: \n\n");	
		for(y=0; y<6; y++){	
			for(x=0; x<6; x++){
			
			printf("a[%d][%d] = ", y, x);
			scanf("%d", &n);
			
			a[y][x]=n;
		}
			
	}
		
		printf("\n\nMatriz digitada: \n\n");			
		for(y=0; y<6; y++){
			for(x=0; x<6; x++){
			
			printf("%2d ", a[y][x]);
		}
			
		printf("\n");	
	}
		break;

		
	case 2:
	k++/ //variavel de controle para indicar a opção valida	
	
	printf("\n\nMatriz sorteada: \n\n");
	for(y=0; y<6; y++){
		for(x=0; x<6; x++){
		
		a[y][x]=rand()%100;	
			printf("%2d ", a[y][x]);
		
		}
		
		printf("\n");		
	}
		break;
	

	default:
		printf("\n\n*Opção invalida!!!*\n\n*Tente Novamente!!!*");
	
}
	
	if(k!=0){
		for(y=0; y<6; y++){
			for(x=0; x<6; x++){
				if(a[y][x]%2!=0){
			
				impares[soma]=a[y][x];				
				soma++;
			
			}			
		}
	}
	
	
		printf("\n\nQuantidade de numeros impares: %d", soma);
		printf("\n\nNúmeros impares da matriz: ");
			
		for(z; z<soma; z++){
			
		printf("%d ", impares[z]);

	}

}
}


//5. Faça um programa para ler, ou preencher com números aleatórios, uma matriz 4 x 4, conte e escreva quantos valores maiores que 10 ela possui.

#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale(LC_ALL, "Portuguese");
	srand(time(NULL));

	int a[4][4], y, x, z=0, j, n, k=0;
	
	printf("Escolha uma das opções a baixo: \n\n1 - Caso queira preencher a matriz digite 1. \n2 - Caso queira que a matriz seja preenciada com números aleatórios digite 2. \n\nSelecione a sua opção: ");
	scanf("%d", &j);
	
	switch(j){
		
	case 1:
		
	k++;//variável de controle para indicar opção válida
		
		printf("\n\nDigite os números para preencher a matriz: \n\n");
		
		for(y=0; y<4; y++){
			
			for(x=0; x<4; x++){
			
			printf("a[%d][%d] = ", y, x);
			scanf("%d", &n);
			
			a[y][x]=n;
		}
			
	}
		
		printf("\n\nMatriz digitada: \n\n");
				
		for(y=0; y<4; y++){
			
			for(x=0; x<4; x++){
			
			printf("%2d ", a[y][x]);
		}
		
		printf("\n");	
	}
		
		break;
		
	case 2:
		
	k++;//variável de controle para indicar opção valida
	
	printf("\n\nMatriz sorteada: \n\n");
	
	for(y=0; y<4; y++){
		
		for(x=0; x<4; x++){
		
		a[y][x]=rand()%30;
				
			printf("%2d ", a[y][x]);
		
		}
		
		printf("\n");
			
	}
	
	break;
	
	default:
		
		printf("\n\n*Opção invalida!!!*\n\n*Tente Novamente!!!*");
	
}

	if (k==1){
	
	printf("\n\nNúmeros maiores que 10: \n\n");
		
			for(y=0; y<4; y++){
			
				for(x=0; x<4; x++){
				
					if(a[y][x]>10){
					
					printf("%d ", a[y][x]);
					
					z++;
				}	
			}
		}
		
				if(z==0){
	
				printf("*Nenhum número sorteado é maior que 10*");		
			}
	}
}


//6. Declare uma matriz 5 x 5. Preencha com 1 a diagonal principal e com 0 os demais elementos. Escreva ao final a matriz obtida.

#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale(LC_ALL, "Portuguese");
	srand(time(NULL));

	int a[5][5], y, x;
	
	printf("Matriz: \n\n");
	
	for(y=0; y<5; y++){
		for(x=0; x<5; x++){
		
		if(y==x){
			
			a[y][x]=1;
		}
		
			else{
				
				a[y][x]=0;
			}
			
		printf("%2d ", a[y][x]);
			
	}		
	
	printf("\n");	
}

}


//7. Faça um programa para ler, ou preencher com números aleatórios, uma matriz 4 x 4. Em seguida, imprima a matriz e retorne a localização (linha e a coluna) do maior valor.

#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale(LC_ALL, "Portuguese");
	srand(time(NULL));

	int a[4][4], y, x, j, n, maior=0, l=0, c=0;
	
	printf("Escolha uma das opções a baixo: \n\n1 - Caso queira preencher a matriz digite 1. \n2 - Caso queira que a matriz seja preenciada com números aleatórios digite 2. \n\nSelecione a sua opção: ");
	scanf("%d", &j);
	
	switch(j){
		
	case 1:
		
		printf("\n\nDigite os números para preencher a matriz: \n\n");	
		for(y=0; y<4; y++){	
			for(x=0; x<4; x++){
			
			printf("a[%d][%d] = ", y, x);
			scanf("%d", &n);
			
			a[y][x]=n;
		}
			
	}
		
		printf("\n\nMatriz digitada: \n\n");			
		for(y=0; y<4; y++){
			for(x=0; x<4; x++){
			
			printf("%2d ", a[y][x]);
		}
		
		printf("\n");	
	}
		
		break;
		
	case 2:
	
	printf("\n\nMatriz Sorteada: \n\n");
	for(y=0; y<4; y++){
		for(x=0; x<4; x++){
		
		a[y][x]=rand()%30;	
			printf("%2d ", a[y][x]);
		
		}
		
		printf("\n");
			
	}
	
	break;
	
	default:
		
		printf("\n\n*Opção invalida!!!*\n\n*Tente Novamente!!!*");
	
}

	for(y=0; y<4; y++){
		for(x=0; x<4; x++){
			if(maior<a[y][x]){
				
				l=y;
				c=x;
				maior=a[y][x];
				
			}
		}
	}
	
	printf("\n\nMaior valor da matriz se encontra na coluna %d e linha %d e é o número %d", c, l, maior);
}



// 8. Faça um programa para ler, ou preencher com números aleatórios, uma matriz 5 x 5. Leia também um valor "X". O programa deverá fazer uma busca desse valor na matriz e, ao final, 
//escrever a localização (linha e coluna) ou uma mensagem de “não encontrado”.
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale(LC_ALL, "Portuguese");
	srand(time(NULL));

	int a[5][5], y, x, j, n, maior=0, v, k=0;
	
	printf("Escolha uma das opções a baixo: \n\n1 - Caso queira preencher a matriz digite 1. \n2 - Caso queira que a matriz seja preenciada com números aleatórios digite 2. \n\nSelecione a sua opção: ");
	scanf("%d", &j);
	
	switch(j){
		
	case 1:
		
		printf("\n\nDigite os números para preencher a matriz: \n\n");	
		for(y=0; y<5; y++){	
			for(x=0; x<5; x++){
			
			printf("a[%d][%d] = ", y, x);
			scanf("%d", &n);
			
			a[y][x]=n;
		}
			
	}
		
		printf("\n\nMatriz digitada: \n\n");			
		for(y=0; y<5; y++){
			for(x=0; x<5; x++){
			
			printf("%2d ", a[y][x]);
		}
			
		printf("\n");	
	}
		break;

		
	case 2:
	
		printf("\n\nMatriz sorteada: \n\n");
		for(y=0; y<5; y++){
			for(x=0; x<5; x++){
			
			a[y][x]=rand()%30;	
				printf("%2d ", a[y][x]);
			
		}
		
		printf("\n");		
	}
		break;
	

	default:
		printf("\n\n*Opção invalida!!!*\n\n*Tente Novamente!!!*");
	
}
	
	
	printf("\n\nDigite o valor que você deseja procurar na matriz: ");
	scanf("%d", &v);
	
	for(y=0; y<5; y++){
		for(x=0; x<5; x++){
			if(a[y][x]==v){
				
				k++;//variavel de controle para contar os numeros iguais ao valor digitado
				printf("\n\nValor '%d' se encontra na linha %d e coluna %d", v, y, x);
				
			}
			
		}
	}
	
	
	if(k==0){
		printf("\n\n*Valor não encontrado!!!*");		
	}
}



//9.Faça um programa para gerar automaticamente números entre 0 e 99 de uma cartela de bingo. Sabendo que cada cartela devera conter 5 linhas de 5 números, 
//gere estes dados de modo a não ter números repetidos dentro das cartelas. O programa deve exibir na tela a cartela gerada.

#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>
#include <string.h>
#include <time.h>

int main (){
	
	setlocale (LC_ALL, "portuguese");
	srand(time(NULL));
	
	int a[5][5], x, y, aux=0, w, z, cartela;
	
	printf("Cartela gerada: \n\n");
	                   
    for(y=0; y<5; y++){
        for(x=0; x<5; x++){
            do{
                cartela = rand() % 99;
            	aux=0;
            	
                for(z=0; z<5; z++){
                    for(w=0; w<5; w++){
                        if(cartela == a[z][w]){
                            aux=1;
						}
                    }
                }
        } while(aux == 1);
            
		a[y][x] = cartela;
		printf("%2d ", a[y][x]);
	}
		printf("\n");
		
	}
}






//10. Faça um programa para ler, ou preencher com números aleatórios, três matrizes 4 x 4. Em seguida, crie uma quarta matriz com os maiores valores de cada posição das matrizes criadas anteriormente.

#include <stdio.h>
#include <string.h>
#include <conio.h>
#include <time.h>
#include <stdlib.h>
#include <locale.h>

int main(){
	
	int a[4][4], b[4][4], c[4][4], y, x;
	srand( time(NULL) );
	
	for(y=0; y<4; y++){
		for(x=0; x<4; x++){
			
			a[y][x]=rand()%50;
			b[y][x]=rand()%50;
			c[y][x]=rand()%50;
			
		}
	}
	
	
	printf("Primeira matriz: \n\n");
	for(y=0; y<4; y++){
		for(x=0; x<4; x++){		
			printf("%2d ", a[y][x]);	
		}	
		printf("\n");
	}
	
	
	printf("\n\nSegunda matriz: \n\n");
	for(y=0; y<4; y++){
		for(x=0; x<4; x++){		
			printf("%2d ", b[y][x]);	
		}	
		printf("\n");
	}
	
	printf("\n\nTerceira matriz: \n\n");
	for(y=0; y<4; y++){
		for(x=0; x<4; x++){		
			printf("%2d ", c[y][x]);	
		}	
		printf("\n");
	}
	
	printf("\n\nQuarta matriz: \n\n");
	for(y=0; y<4; y++){
		for(x=0; x<4; x++){
			
			if(a[y][x]>b[y][x] && a[y][x]> c[y][x]){
				
				printf("%2d ", a[y][x]);
			}
			
				else if(b[y][x]>a[y][x] && b[y][x]> c[y][x]){
				
				printf("%2d ", b[y][x]);
			}
			
				else if(c[y][x]>b[y][x] && c[y][x]> a[y][x]){
				
				printf("%2d ", c[y][x]);
			}
			
				else if(c[y][x]==b[y][x] && c[y][x]==a[y][x]){
				
				printf("%2d ", c[y][x]);
			}
			
				else if(c[y][x]==b[y][x] && c[y][x]>a[y][x]){
				
				printf("%2d ", c[y][x]);
			}
			
				else if(a[y][x]==b[y][x] && a[y][x]>c[y][x]){
				
				printf("%2d ", a[y][x]);
			}
			
				else if(a[y][x]==c[y][x] && a[y][x]>b[y][x]){
				
				printf("%2d ", a[y][x]);
			}
			
		}
		
		printf("\n");
	}	
}
