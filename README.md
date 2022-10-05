# TemperatureConverter
A simple temperature converter working on calling methods outside the main class & using user input & if statements
-------------------------------------------------------------------------------------------------------------------



import java.util.Scanner;

public class TempConvert {

	public static void main(String[] args) {
		
		Scanner scanner = new Scanner(System.in);
		System.out.println("Welcome to the temperature converter.\n");
		System.out.println("1. Celsius to Kelvin");
		System.out.println("2. Kelvin to Celsius");
		System.out.println("3. Fahrenheit to Celsius");
		System.out.println("4. Celsius to Fahrenheit");
		System.out.println("5. Fahrenheit to Kelvin");
		System.out.println("6. Kelvin to Fahrenheit\n");
		int mode;
		
    // will continue continue to ask user for moode until a correct mode is selected
		do{
			System.out.print("Please select a mode by typing the corresponding number: ");
			mode = scanner.nextInt();
		
		}while(mode != 1 && mode != 2 && mode != 3 && mode != 4 && mode != 5 && mode != 6);
		
		if(mode == 1) {
			CelKel();
		}
		
		if(mode == 2) {
			CelKel();
		}
		
		if(mode == 3) {
			FahCel();
		}
		
		if(mode == 4) {
			CelFah();
		}
		
		if(mode == 5) {
			FahKel();
		}
		
		if(mode == 6) {
			KelFah();
		}
		
		scanner.close();
		

	}
	
	static void CelKel() {
		//Celsius to Kelvin
		System.out.print("Please enter the Celcius value: ");
		Scanner Temp = new Scanner(System.in);
		double OldTemp = Temp.nextFloat();
		double NewTemp = OldTemp + 273.15;
		System.out.printf("The value in Kelvin is: %.2f", NewTemp);
		Temp.close();
		
	}
	
	static void KelCel() {
		//Kelvin to Celsius
		System.out.print("Please enter the Kelvin value: ");
		Scanner Temp = new Scanner(System.in);
		double OldTemp = Temp.nextFloat();
		double NewTemp = OldTemp - 273.15;
		System.out.printf("The value in Celsius is: %.2f", NewTemp);
		Temp.close();
		
	}
	
	static void FahCel() {
		//Fahrenheit to Celsius
		System.out.print("Please enter the Fahrenheit value: ");
		Scanner Temp = new Scanner(System.in);
		double OldTemp = Temp.nextFloat();
		double NewTemp = (OldTemp - 32) * 5/9;
		System.out.printf("The value in Celsius is: %.2f", NewTemp);
		Temp.close();
		
	}
	
	static void CelFah() {
		//Celsius to Fahrenheit
		System.out.print("Please enter the Celsius value: ");
		Scanner Temp = new Scanner(System.in);
		double OldTemp = Temp.nextFloat();
		double NewTemp = OldTemp * (9/5) + 32;
		System.out.printf("The value in Fahrenheit is: %.2f", NewTemp);
		Temp.close();
		
	}
	
	static void FahKel() {
		//Fahrenheit to Kelvin
		System.out.print("Please enter the Fahrenheit value: ");
		Scanner Temp = new Scanner(System.in);
		double OldTemp = Temp.nextFloat();
		double NewTemp = (OldTemp-32) * 5/9 + 273.15;
		System.out.printf("The value in Kelvin is: %.2f", NewTemp);
		Temp.close();
		
	}
	
	static void KelFah() {
		//Kelvin to Fahrenheit
		System.out.print("Please enter the Kelvin value: ");
		Scanner Temp = new Scanner(System.in);
		double OldTemp = Temp.nextFloat();
		double NewTemp = (OldTemp-273.15) * 9/5 + 32;
		System.out.printf("The value in Fahrenheit is: %.2f", NewTemp);
		Temp.close();
		
	}
}
