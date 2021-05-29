# Algoritimos-em-Java
import java.util.Scanner;
public class exerc13L05grupo2 {

	public static void main(String[] args) {
		@SuppressWarnings("resource")
		Scanner in = new Scanner(System.in); //comando_necessário para_a leitura_de_dados

		// TODO Auto-generated method stub

		/*
	 	* TESTE REALIZADO :
	 	* 
	  	Digite o nome do 1° funcionário :
		lucas
		Digite o 1° salário :
		1750
		O funcionário lucas terá aumento de R$ 175.0
		e passará a receber R$ 1925.0000000000002
		-------------------------------------------------------
		Deseja calcular o salário de mais funcionários ? 
		digite S para sim N para não :
		s
		Digite o nome do 3° funcionário :
		joao
		Digite o 3° salário :
		1900
		O funcionário joao terá aumento de R$ 95.0
		e passará a receber R$ 1995.0
		-------------------------------------------------------
		Deseja calcular o salário de mais funcionários ? 
		digite S para sim N para não :
		n
		Programa encerrado 
	 
	 	********************************************************************************************************
	 	
	 	O programa não faz tratamento para caso o usuário digitar um valor diferente
	 	de 's' ou 'S' que nem é exibido no teste abaixo :
	 
	  	Digite o nome do 1° funcionário :
		fred
		Digite o 1° salário :
		1250
		O funcionário fred terá aumento de R$ 187.5
		e passará a receber R$ 1437.5
		-------------------------------------------------------
		Deseja calcular o salário de mais funcionários ? 
		digite S para sim N para não :
		f
		Programa encerrado
	 	*
	 	*
	 	*/
	char repetição = 's' ;	//variavel do tipo char declarada
	int cont = 1 ;	//variavel contadora declarada
	
	while(repetição == 's' || repetição == 'S')	//loop para o programa repetir 
												//enquanto variavel char receber 's' ou 'S'
	{
		
		System.out.println("Digite o nome do "+cont+"° funcionário :");	//imprime mensagem na tela
		String nome = in.next();	//faz a leitura do nome do funcionário
		System.out.println("Digite o "+cont+"° salário :");	//imprime mensagem na tela perguntando o salário
		double salario = in.nextInt();	//faz a leitura da variavel salário
		double aumento = 0 ;	//variavel do tipo double sendo inicializada com zero
		
		/*
		 * caso salário seja menor ou igual a 900 o if abaixo será validado
		 * 
		 */
		
		
		if(salario <= 900)	//
		
		{
			aumento = salario * 0.2 ;	//variavel aumento recebe 20% do valor de salario
			salario = salario * 1.2 ;	//variavel salario recebe seu valor mais 20%
			
			}else
				/*
				 * caso salário seja maior que 900 e menor/igual a 1300 o if abaixo é validado
				 * 
				 */
				
				if(salario > 900 && salario <= 1300) {
					aumento = salario * 0.15 ;	//variavel aumento recebe 15% do valor de salario
					salario = salario * 1.15 ;	//variavel salario recebe seu valor mais 15%
					
				}else
					/*
					 * caso salário seja maior que 1300 e menor/igual a 1800 o if abaixo é validado
					 * 
					 */
					if(salario > 1300 && salario <= 1800) {
						aumento = salario * 0.1 ;	//variavel aumento recebe 10% do valor de salario
						salario = salario * 1.1 ;	//variavel salario recebe seu valor mais 10%
						
						}else
							/*
							 * caso salário seja maior que 1800 o if abaixo é validado
							 * 
							 */
							if(salario > 1800) {
								aumento = salario * 0.05 ;	//variavel aumento recebe 0.05% do valor de salario
								salario = salario * 1.05 ;	//variavel salario recebe seu valor mais 0.05%
							}
		
		
		/* Nas linhas abaixo é a parte do código que irá imprimir na tela
		 * o salário calculado mais o nome do funcionário que foi digitado
		 * 
		 */
		
		
		System.out.println("O funcionário "+nome+ " terá aumento de R$ "+aumento+"\n"	//imprime mensagem na tela
				+ "e passará a receber R$ "+salario);	//imprime mensagem na tela
		
		cont = cont + 1 ;	//variavel contadora recebe + 1
		
		
		System.out.println("-------------------------------------------------------");
		
		/*
		 * Nas linhas abaixo será perguntando se o usuário deseja continuar o programa
		 * 
		 */
		
		System.out.println("Deseja calcular o salário de mais funcionários ? ");	//imprime mensagem na tela
		System.out.println("digite S para sim N para não :");	//imprime mensagem na tela 
		repetição = in.next().charAt(0);	//será lido o valor que a variável char irá receber
		
		
	
		}
			
			System.out.println("Programa encerrado");	//imprime mensagem na tela
	}
}

	
