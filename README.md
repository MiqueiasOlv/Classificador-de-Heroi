Classificador de Heroi

classificadordeheroi.java
import java.util.Scanner;

public class ClassificadorHeroi {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Entrada de dados
        System.out.print("Digite o nome do herói: thor   ");
        String nome = scanner.nextLine();

        System.out.print("Digite a quantidade de XP:8500 ");
        int xp = scanner.nextInt();

        String nivel;

        // Estrutura de decisão      
        if (xp < 1000) {
            nivel = "Ferro";
        } else if (xp <= 2000) {
            nivel = "Bronze";
        } else if (xp <= 5000) {
            nivel = "Prata";
        } else if (xp <= 7000) {
            nivel = "Ouro";
        } else if (xp <= 8000) {
            nivel = "Platina";
        } else if (xp <= 9000) {
            nivel = "Ascendente";
        } else if (xp <= 10000) {
            nivel = "Imortal";
        } else {
            nivel = "Radiante";
        }

        // Saída
        System.out.println("O Herói de nome " + nome + " está no nível de " + nivel);

        scanner.close();
    }
}
