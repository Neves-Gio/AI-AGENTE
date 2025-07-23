
---

# 🇺🇸 American Visa Agent - Java Console App

Este é um mini agente inteligente feito em Java para simular uma conversa com um usuário interessado no visto americano de turismo (B1/B2).  
Projeto criado por Giovanni Neves 🎯

## 💻 Tecnologias
- Java 11+
- Programação orientada a objetos
- Console I/O

## 🚀 Como usar

```bash
javac src/Main.java
java src/Main
👤 Olá! Bem-vindo ao Agente de Visto Americano.
Digite seu nome: João
Oi João! Qual o seu objetivo com o visto? (turismo, negócios, ambos)
> turismo
Legal! Já teve visto antes? (sim/não)
> não
Entendi. Vamos te ajudar a conseguir seu primeiro visto! 🇺🇸
### 🧠 `Main.java` (coloque dentro da pasta `src`)

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("👤 Olá! Bem-vindo ao Agente de Visto Americano.");
        
        System.out.print("Digite seu nome: ");
        String nome = input.nextLine();

        System.out.printf("Oi %s! Qual o seu objetivo com o visto? (turismo, negócios, ambos)\n> ", nome);
        String objetivo = input.nextLine().toLowerCase();

        System.out.print("Já teve visto antes? (sim/não)\n> ");
        String teveVistoAntes = input.nextLine().toLowerCase();

        System.out.println("\n🔎 Analisando informações...");
        System.out.println("--------------------------------------");

        if (teveVistoAntes.equals("sim")) {
            System.out.printf("Perfeito, %s! Podemos ajudar no processo de renovação do seu visto para %s!\n", nome, objetivo);
        } else {
            System.out.printf("Entendi. Vamos te ajudar a conseguir seu primeiro visto para %s! 🇺🇸\n", objetivo);
        }

        System.out.println("📅 Em breve, um de nossos consultores entrará em contato.");
        System.out.println("Obrigado por utilizar nosso agente virtual!");
        System.out.println("--------------------------------------");

        input.close();
    }
}
# AI-AGENTE
