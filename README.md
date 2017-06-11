# ObliczanieSt-e-

import java.util.InputMismatchException;
import java.util.Scanner;

public class ObliczanieStężeńZWyborem
{

	public static void main(String[] args)
	{
		System.out.println("Aby obliczyć:\n- stężenie roztworu podaj \"CP\":\n- stężenie molowe podaj \"CM\": ");
		Scanner input = new Scanner(System.in);
		while (input.hasNextLine())
		{
			String decision = input.nextLine();
			switch (decision)
			{
			case "CP":
				Scanner in = new Scanner(System.in);
				//Roztwór roztwór = new Roztwór();
				System.out.println("Podaj:");
				System.out.println("- ilość rozpuszczalnika (bez jednostki): ");
				double ilośćRozp = input.nextDouble();
				System.out.println("- ilość substancji rozpuszczonej (bez jednostki):");
				double ilośćSubRozp = input.nextDouble();
				System.out.println("Podaj kolejno jednostki(eg. KG G), (rozpuszczalnika, sub. rozpuszczonej): ");
				String wybór1 = in.nextLine();

				System.out.println("Stężenie procentowe roztworu wynosi: ");
				switch (wybór1)
				{
				case "G G":
					double obliczCPGG = ilośćSubRozp / ilośćRozp * 100;
					System.out.print(obliczCPGG + " %");
					if (obliczCPGG < 100){
						System.out.print(" - Roztwór nienasycony.\n");
					}
					if (obliczCPGG > 100){
						System.out.print(" - Roztwór przesycony.\n");
					}
					if (obliczCPGG == 100){
						System.out.print(" - Roztwór nasycony.\n");
					}
					break;
				case "KG KG":
					double obliczCPKGKG = ilośćSubRozp / ilośćRozp * 100;
					System.out.print(obliczCPKGKG + " %");
					if (obliczCPKGKG < 100){
						System.out.print(" - Roztwór nienasycony.\n");
					}
					if (obliczCPKGKG > 100){
						System.out.print(" - Roztwór przesycony.\n");
					}
					if (obliczCPKGKG == 100){
						System.out.print(" - Roztwór nasycony.\n");
					}
					break;
				case "KG G":

					double obliczCPKgG = ilośćSubRozp / (ilośćRozp * 1000) * 100;
					System.out.print(obliczCPKgG + " %");
					if (obliczCPKgG < 100){
						System.out.print(" - Roztwór nienasycony.\n");
					}
					if (obliczCPKgG > 100){
						System.out.print(" - Roztwór przesycony.\n");
					}
					if (obliczCPKgG == 100){
						System.out.print(" - Roztwór nasycony.\n");
					}
					break;
				case "G KG":
					double obliczCPGKg = (ilośćSubRozp * 1000) / ilośćRozp * 100;
					System.out.print(obliczCPGKg + " %");
					if (obliczCPGKg < 100){
						System.out.print(" - Roztwór nienasycony.\n");
					}
					if (obliczCPGKg > 100){
						System.out.print(" - Roztwór przesycony.\n");
					}
					if (obliczCPGKg == 100){
						System.out.print(" - Roztwór nasycony.\n");
					}
					break;
				}
				break;
			case "CM":
				Scanner inn= new Scanner(System.in);
				System.out.println("Podaj:");
				System.out.println("- liczbę moli (bez jednostki): ");
				double liczbaMoli = input.nextDouble();
				System.out.println("- objętość (bez jednostki):");
				double objętość = input.nextDouble();
				//Roztwór roztwór = new Roztwór();
				System.out.println("Podaj kolejno jednostki(eg. MMOL CM^3), (moli, objętości): ");
				String wybór2= inn.nextLine();
				System.out.println("Stężenie molowe roztworu wynosi: ");
				
				switch(wybór2){
				case "MOL CM^3":
					double obliczCMMOLCM3= liczbaMoli/(objętość*0.001);
					System.out.println(obliczCMMOLCM3 + " mol/dm^3");
					break;
				case "MMOL CM^3":
					double obliczCMMMOLCM3= (liczbaMoli*0.001)/(objętość*0.001);
					System.out.println(obliczCMMMOLCM3 + " mol/dm^3");
					break;
				case "KMOL CM^3":
					double obliczCMKMOLCM3= (liczbaMoli*1000)/(objętość*0.001);
					System.out.println(obliczCMKMOLCM3 + " mol/dm^3");
					break;
				case "MOL DM^3":
					double obliczCMMOLDM3= liczbaMoli/objętość;
					System.out.println(obliczCMMOLDM3 + " mol/dm^3");
					break;
				case "MMOL DM^3":
					double obliczCMMMOLDM3= (liczbaMoli*0.001)/objętość;
					System.out.println(obliczCMMMOLDM3 + " mol/dm^3");
					break;
				case "KMOL DM^3":
					double obliczCMKMOLDM3= (liczbaMoli*1000)/objętość;
					System.out.println(obliczCMKMOLDM3 + " mol/dm^3");
					break;
				}
			}
		}

	}
}
