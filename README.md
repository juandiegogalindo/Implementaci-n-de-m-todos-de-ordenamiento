# Implementaciòn de mètodos de ordenamiento
Insertion sort

public class InsertionSortMain {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        int[] arreglo = new int[5];

        Scanner sc = new Scanner(System.in);

        for (int i = 0; i < arreglo.length; i++) {
            System.out.print("Agregue un elemento al arreglo: ");
            arreglo[i] = sc.nextInt();
        }
        
        for (int i = 0; i < arreglo.length; i++) {
            System.out.print("[" + arreglo[i] + "]");
        }
        System.out.println("");

        int n = arreglo.length;
        for (int j = 1; j < n; j++) {
            int key = arreglo[j];
            int i = j - 1;
            while ((i > -1) && (arreglo[i] > key)) {
                arreglo[i + 1] = arreglo[i];
                i--;
            }
            arreglo[i + 1] = key;
        }
        
        System.out.print("Despues: ");
        for (int i = 0; i < arreglo.length; i++) {
            System.out.print("[" + arreglo[i] + "]");
        }
    }
}
