# Programacao-de-Solucoes-Computacionais-Ex12-Lista05
Embaralha palavra.
import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collections;
import java.util.Scanner;

public class Ex12 {
    public static void main(String[] args) throws Exception {
        String palavraEmbaralhada = "";
        Scanner sc = new Scanner(System.in);
        System.out.println("Informe uma palavra: ");
        String palavra = sc.next();

        sc.close();
        String[] arrayString = palavra.split("");

        ArrayList<String> strList = new ArrayList<String>(Arrays.asList(arrayString));

        Collections.shuffle(strList);

        for (String letter : strList) {
            palavraEmbaralhada += letter.toUpperCase();
        }
        System.out.println(palavraEmbaralhada);
    }

    public static int rand(int min, int max) {
        int randomNum = (int) Math.floor(Math.random() * (max - min + 1)) + min;
        return randomNum;
    }
}
