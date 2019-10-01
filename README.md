# EXERCICIO-LISTA-03

QUESTÃO 01


#include <stdio.h>

int main(){
	
	char n[50], i;
	
	printf("Digite algo para saber quando caracteres o texto possui: ");
	gets(n);

	for(i= 0; i < sizeof(n) && n[i]!='\0'; i++);
	printf("%d", i);
}



QUESTÃO 02
#include <stdio.h>

int main(){
	
	int i, vog = 0;
	char name[100];
	
	printf("Digite aqui um texto para saber a quantidade de vogais existente no texto digitado: ", name);
	gets(name);
	
	for(i= 0; i<= sizeof(name) && name[i] != '\0'; i++){
		if(name[i] =='a' || name[i] =='e' || name[i] =='i' || name[i] =='o' || name[i] =='u' || name[i] =='A' || name[i] =='E' || name[i] =='I' || name[i] =='O' || name[i] =='U' ) {
			vog++;
		}
	}
	
	printf("quantidade de vogais = %d", vog);
	
}



QUESTÃO 03

#include <stdio.h>
#include <locale.h>

	int i,ig,dif;
	char text1[255], text2[255];
int main(){
	
	setlocale(LC_ALL,"Portuguese");
	

	printf("Compare o texto 1 com o texto 2 para saber se são iguais: \n");
	printf("texto 1 : ", text1);
	gets(text1);
	printf("texto 2 : ", text2);
	gets(text2);
	
	for (i = 0;i <= sizeof(text1) && text1[i] != '\0';i++){
		if (text1[i] == text2[i]){
			ig=1;
		}
		else{
			dif=1;
		}
	}
	if (dif == 1){
		printf("Textos diferentes");
	}else{
		printf("Textos iguais");
	}
	return 0;
}

QUESTÃO 04

#include <stdio.h>
#include <locale.h>

int i;
char text1[255], text2[255];

int main(){
	setlocale(LC_ALL,"Portuguese");
	
	printf("Digite algo: ");
	gets(text1);

	for (i = 0;i<sizeof(text1) && text1[i]!='\0';i++){
		text2[i]= text1[i];
	}
	printf("Você digitou: %s", text2);
}


QUESTÃO 05

#include <stdio.h>
#include <locale.h>


char string1[255],string2[255];
int i, j;

int main(){
	setlocale(LC_ALL,"Portuguese");
	
	printf("<---------------------CONCATENANDO AS STRINGS-----------------------> \n");
	printf("Digite algo:");
	gets(string1);
	printf("Digite algo:");
	gets(string2);
	
	for(i = 0;string1[i] != '\0';i++);

	for(j = 0;j<=sizeof(string2) &&  string2[j]!='\0';j++,i++){
		string1[i] = string2[j];
			
	}
	string1[i]='\0';
 	printf("Parabéns você concatenou as strings: %s ",string1);
}
