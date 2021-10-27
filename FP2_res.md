**UNIVERSIDADE LUSÓFONA DE HUMANIDADES E TECNOLOGIAS**


1. Implemente um programa que escreve no ecrã a frase "O primeiro programa nunca se esquece!".

   *Resolução:*

   ```c
   void ex1 (void) {
       printf("\n\t******** Exercicio 1 ********\n");
       printf("O primeiro programa nunca se esquece!\n");
   }
   ```

2. O que faz o seguinte programa?

   ```c
   #include <stdio.h>
   
   int main(void)
   {
   	int x;
   	scanf( "%d", &x );
   	printf("%d\n", 2*x );
   	return 0;
   }
   ```

*Resolução: Lê um valor inteiro do teclado e imprime o valor multiplicado por 2.* 


3. Leia uma temperatura em graus Fahrenheit e apresente-a convertida em graus Celsius. A fórmula de conversão é: C = 5.0 ∗ (F − 32.0)/9.0, sendo C é a temperatura em graus Celsius e F a temperatura em graus Fahrenheit. 

   *Resolução:*

   ```c
   void ex3(void) {
   	float celsius,fahrenheit;
   	printf("\n\t******** Exercicio 3 ********\n");
   	printf("Insira a temperatura (graus Fahrenheit):\n");
   	scanf("%f", &fahrenheit);
   	celsius = 5.0 * (fahrenheit - 32.0)/9.0;
   	printf("A temperatura em Graus Celsius é de %f\n", celsius);
   }
   ```

2. Leia o valor do raio de um círculo. Calcule e imprima a área do círculo correspondente. A área do círculo é π ∗ raio² , considere π = 3.141592 (constante). 

   *Resolução:*

   ```c
   void ex4(void) {
   	const float Pi = 3.14F;
   	float raio, area;
   	printf("\n\t******** Exercicio 4 ********\n");
   	printf("Inira o raio de um círculo:\n");
   	scanf("%f", &raio);
   	area = Pi * (raio*raio);
   	printf("O valor da área do circulo é de %f\n", area);
   }
   ```

3. Faça um programa que peça ao utilizador 2 valores inteiros e coloque o primeiro valor numa variável chamada de A e o segundo valor noutra variável chamada de B. Em seguida, o seu programa deverá trocar o conteúdo destas variáveis e imprimir no ecrã o que cada variável contém.
   *Resolução:*

   ```c
   void ex5(void) {
   	int a, b, aux;
   	printf("\n\t******** Exercicio 5 ********\n");
   	printf("Insira um valor para a variável 'A':\n");
   	scanf("%d", &a);
   	printf("Insira um valor para a variável 'B':\n");
   	scanf("%d", &b);
   	printf("O valor inserido para a variável 'A' foi %d\n", a);
   	printf("O valor inserido para a variável 'B' foi %d\n", b);	
   
   	aux = a;
   	a = b;
   	b = aux;
   	puts("Depois da troca:");
   	printf("variável 'A': %d\n", a);
   	printf("variável 'B': %d\n", b);
   }
   ```
   
4. Faça um programa que peça ao utilizador 4 valores inteiros. Coloque estes valores nas variáveis a, b, c, d e imprima no ecrã o resultado da seguinte expressão:(a + b + c) x d
   *Resolução:*

   ```c
   void ex6(void) {
   	int a, b, c, d;
   	printf("\n\t******** Exercicio 6 ********\n");    
   	printf("Insira quatro numeros separados por virgula(',')\n");
   	scanf("%d,%d,%d,%d",&a,&b,&c,&d);
   	printf("o resultado da operação (a + b + c) * d) é: %d\n",(a + b + c) * d);
   }
   ```
   
5. Faça um programa que peça ao utilizador 4 notas de um aluno e imprima no ecrã a média desse aluno. 
   *Resolução:*

   ```c
   void ex7(void) {
   	float nota1, nota2, nota3, nota4, media;
       printf("\n\t******** Exercicio 7 ********\n");    
   	printf("Insira o valor da primeira nota:\n");
   	scanf("%f", &nota1);
   	printf("Insira o valor da segunda nota:\n");
   	scanf("%f", &nota2);
   	printf("Insira o valor da terceira nota:\n");
   	scanf("%f", &nota3);
   	printf("Insira o valor da quarta nota:\n");
	scanf("%f", &nota4);
   	media = (nota1+nota2+nota3+nota4)/4;
   	printf("O valor da média das notas é: %f\n", media);
   }
   ```
   
8. Considere um programa com as seguintes variáveis e respetivas inicializações:

    `unsigned char c = 3.14;` 
    `unsigned short int i = 3.14; `
    `unsigned int j = ‘B’; `
    `float f = ‘C’; `

    Usando o debugger (sem recorrer a printf()) verifique:

    - Qual é o valor efetivo f?

    - Qual o valor das variáveis quando se soma o valor 2 a cada uma delas?

    *Resolução:*

    ```c
    void ex8 (void) {
    	unsigned char c = 3.14;
    	unsigned short int i = 3.14;
    	unsigned int j = 'B';
    	float f = 'C';
    	printf("\n\t******** Exercicio 8 ********\n");
    	/* Usar o Debug e em "Debugging windows" abrir "Watches"*/
    	c = c + 2;
    	i = i + 2;
    	j = j + 2;
    	f = f + 2;
    }
    ```

9. Faça um programa que, a partir da leitura  das medidas dos lados de um retângulo (comprimento e largura), lidos do teclado, calcule e imprima a área e o perímetro do retângulo.
   *Resolução:*

   ```c
   void ex9(void){
   	int comp,larg;
   	printf("\n\t******** Exercicio 9 ********\n");    
   	printf("Insira o comprimento do retângulo:\n");
   	scanf("%d", &comp);
   	printf("Insira a largura do retângulo:\n");
   	scanf("%d", &larg);
   	printf("A área do retângulo é: %d\n", comp*larg);
   	printf("O perímetro é: %d\n", 2*(comp + larg));
   }
   ```

10. Faça um programa que leia pelo teclado um valor, em euros, converta e imprima o mesmo num valor     em dólares. Considere que €1 seja equivalente a US$ 1,23.
   *Resolução:*

   ```c
   void ex10(void){
   	float euros, dolares;
   	printf("\n\t******** Exercicio 10 ********\n");    
   	printf("Insira o valor em euros:\n");
   	scanf("%f", &euros);
   	dolares = euros*1.23;
       // imprimir com duas casas decimais (2 caracteres depois da virgula)
   	printf("O valor em dolares é: %.2f", dolares);
   }
   ```

11. A condição física de uma pessoa pode ser medida com base no cálculo do Índice de Massa Corporal     (IMC). O mesmo é calculado dividindo-se o peso desta pessoa em kg pelo quadrado da sua altura em m. Escreva um programa que leia o peso em kilograma e a altura de uma pessoa em metros, calcule e mostre o IMC. 

    *Se as entradas fossem 70.0kg para o peso e 1.80m para altura então a saída esperada seria aproximadamente 21.60.*
    *Resolução:*

    ```c
    void ex11(void){
    	float peso, altura, imc;
    	puts("\n\t******** Exercicio 11 ********");    
    	puts("Insira o seu peso (Kg):");
    	scanf("%f", &peso);
    	puts("Insira a sua altura (m):");
    	scanf("%f", &altura);
    	imc = peso/(altura*altura);
    	printf("O Índice de Massa Corporal (IMC) é de %.2f\n", imc);
    }
    ```

12. Escreva um programa que lê um certo número de segundos e dá o correspondente aos Dias, Horas, Minutos e Segundos.

     *Exemplo: 228184 segundos correspondem a 2 Dias e 15 Horas 23 Minutos e 4 Segundos.*

     *Resolução:*

   ```c
void ex12(void){
	int inputSeconds, inputSecondsCopy;
	int days, hours, minutes, seconds;
	puts("\n\t******** Exercicio 12 ********");
	puts("Insira o numero de segundos");
	scanf("%d", &inputSeconds);
	inputSecondsCopy = inputSeconds;

	// dividir pelo numero de segundos de 1 dia
	// um dia tem 24h e cada hora tem 60*60 segundos
	days = inputSeconds / (24 * 3600);

	// Calculo do resto da divisao anterior para saber quantos segundos sobram
	inputSeconds = inputSeconds % (24 * 3600);
	// Conversao dos segundos que sobrarm para horas
	hours = inputSeconds / 3600; 

	// Calculo do resto da divisao anterior para saber quantos segundos sobram
	inputSeconds %= 3600;
	// Conversao dos segundos que sobrarm para minutos
	minutes = inputSeconds / 60 ; 

	// Calculo do resto da divisao anterior para saber quantos segundos sobram
	inputSeconds %= 60; 
	seconds = inputSeconds; 

	printf("%d segundos correspondem a %d Dias e %d Horas %d Minutos e %d Segundos.\n", 		inputSecondsCopy, days, hours, minutes, seconds);
}
   ```

11. A importância de €780.000,00 será dividida entre três vencedores de um concurso. Sendo que da quantia total:

    - O primeiro vencedor receberá 46%

    - O segundo receberá 32%

    - O terceiro receberá o restante

    Calcule e imprima a quantia ganha por cada um dos vencedores.

   *Resolução:*

   ```c
#define FIRST_FACTOR 0.46
#define SECOND_FACTOR 0.32
#define THIRD_FACTOR (1-(FIRST_FACTOR + SECOND_FACTOR))
void ex13 (void){
	const float premio = 780000.00;
	float primeiro_premio = premio * FIRST_FACTOR;
	float segundo_premio = premio * SECOND_FACTOR;
	float terceiro_premio = premio * THIRD_FACTOR;
	puts("\n\t******** Exercicio 13 ********");
	printf("O valor do primeiro prémio é de %.2f euros.\n", primeiro_premio);
	printf("O valor do segundo prémio é de %.2f euros.\n", segundo_premio);
	printf("O valor do terceiro prémio é de %.2f euros.\n", terceiro_premio);
}
   ```

 

*Função main que chama todas as funções definidas:*

   ```c
#include <stdio.h>

void ex1 (void);
void ex2 (void);
void ex3 (void);
void ex4 (void);
void ex5 (void);
void ex6 (void);
void ex7 (void);
void ex8 (void);
void ex9 (void);
void ex10 (void);
void ex11 (void);
void ex12 (void);
void ex13 (void);
void ex14 (void);

int main (void)
{
	ex1();
	ex2();
	ex3();
	ex4();
	ex5();
	ex6();
	ex7();
	ex8();
	ex9();
	ex10();
	ex11();
	ex12();
	ex13();
	ex14();
	return 0;
}
   ```

 
