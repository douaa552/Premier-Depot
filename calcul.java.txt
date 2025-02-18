package exercice;

public class calculatrice {
	
	public double addition(double a,double b) {
		return a+b;
	}
	public double soustraction(double a,double b) {
		return a-b;
	}
	public double multiplication(double a,double b) {
		return a*b;
	}
	public double division(double a, double b) {
	    if (b == 0) {
	        throw new ArithmeticException("Erreur : division par zéro");
	    }
	    return a / b;
	}
}
package exercice;
import java.util.Scanner;
public class Test {

	public static void main(String[] args) {
		calculatrice c=new calculatrice();
		Scanner S = new Scanner(System.in);
		System.out.println("entrez le premier nombre:");
		double a=S.nextDouble();
		System.out.println("entrez le second nombre:");
		double b=S.nextDouble();
		System.out.println("entrez votre choix:");
		int choix =S.nextInt();
		double resultat=0;
		switch(choix) {
		case 1:
			resultat=c.addition(a,b);
			System.out.println("resultat de l'addition:"+resultat);
			break;
		case 2:
			resultat=c.soustraction(a, b);
			System.out.println("le resultat de la soustraction:"+resultat);
			break;
		case 3:
			resultat=c.multiplication(a, b);
			System.out.println("le resultat de la multiplication:"+resultat);
			break;
		case 4:
			resultat=c.division(a, b);
			System.out.println("le resultat de la division:"+resultat);
			break;
		default:
			System.out.println("choix invalide.");
		}
		
	

	}

}
