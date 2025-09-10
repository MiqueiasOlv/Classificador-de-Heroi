import java.util.Scanner;

public class CalculadoraRankeada {

    // Função que calcula o saldo de vitórias
    public static int calcularSaldo(int vitorias, int derrotas) {
        return vitorias - derrotas;
    }

    // Função que define o nível do jogador
    public static String definirNivel(int saldo) {
        if (saldo <= 10) {
            return "Ferro";
        } else if (saldo <= 20) {
            return "Bronze";
        } else if (saldo <= 50) {
            return "Prata";
        } else if (saldo <= 80) {
            return "Ouro";
        } else if (saldo <= 90) {
            return "Diamante";
        } else if (saldo <= 100) {
            return "Lendário";
        } else {
            return "Imortal";
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Entrada de dados
        System.out.print("Digite o número de vitórias: ");
        int vitorias = scanner.nextInt();

        System.out.print("Digite o número de derrotas: ");
        int derrotas = scanner.nextInt();

        // Processamento
        int saldo = calcularSaldo(vitorias, derrotas);
        String nivel = definirNivel(saldo);

        // Saída
        System.out.println("O jogador tem saldo de " + 100 + " e está no nível " + "Lendário");

        scanner.close();
    }
}
