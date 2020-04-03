# practica1
package clases.pkg3;
import java.util.Scanner;
public class Clases3 {

    private static int i;

    public static void main(String[] args) {
        Scanner Leer = new Scanner(System.in);

        System.out.println("-------tamaño del vector-------");
        int n = Leer.nextInt();

        int opt;
        int tope = 0;
        char[] datos = new char[n];

        System.out.println("-------elija una opcion -------------");
        do {

            System.out.println("1-agregar \n");
            System.out.println("2-mostrar \n");
            System.out.println("3-eliminar \n");
            System.out.println("5-salir\n");
            opt = Leer.nextInt();
            switch (opt) {

                case 1:
                    if (tope < n) {
                        System.out.println("---------agregar datos: ------------\n");

                        System.out.println("digite un caracter");
                        datos[tope] = Leer.next().charAt(0);

                        tope++;

                    } else {
                        System.out.println("pila llena");
                    }
                    break;

                case 2:
                    if (tope > 0) {

                        System.out.println("LOS DATOS SON: ");

                        for (i = tope - 1; i >= 0; i--) {
                            System.out.println("  " + datos[i]);

                        }

                    } else {
                        System.out.println("pila vacía ");

                    }

                    break;
                case 3:
                    tope--;

                    break;
                default:
                    System.out.println("no está en el rango\n -----eliga otra opcion");
            }
        } while (opt != 5);
    }
}
