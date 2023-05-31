package CadastroDeItens;
import java.util.ArrayList;
import java.util.Scanner;

public class CadastroDeItens {

	public static void main(String[] args) {
		 ArrayList<String> listaDeItens = new ArrayList<String>(); // criando uma nova lista de itens
	      
		 	
	        Scanner scanner = new Scanner(System.in); // criando um objeto Scanner para receber entradas do usuário
	        
	        int opcao = 0; // inicializando a opção escolhida pelo usuário
	        
	        while (opcao != 4) { // enquanto a opção escolhida não for 4 (sair), o programa continua executando
	            
	            // mostrando as opções para o usuário
	        	System.out.println();
	        	System.out.println("CADASTRO PARA COMBATE AO HIV");
	        	System.out.println();
	            System.out.println("Selecione a Opcao que deseja:");
	            System.out.println("1 - Cadastrar Paciente");
	            System.out.println("2 - Excluir Paciente");
	            System.out.println("3 - Imprimir lista dos Pacientes");
	            System.out.println("4 - Fechar");
	            
	            opcao = scanner.nextInt(); // lendo a opção escolhida pelo usuário
	            
	            switch (opcao) {
	                
	                case 1:
	                    System.out.println("Digite o nome do Paciente a ser cadastrado:");
	                    String novoItem = scanner.next(); // lendo o nome do paciente a ser cadastrado
	                    listaDeItens.add(novoItem); // adicionando o novo item à lista
	                    System.out.println("Paciente cadastrado com sucesso!");
	                    break;
	                
	                case 2:
	                    System.out.println("Digite o nome do Paciente a ser Excluido:");
	                    String itemDeletado = scanner.next(); // lendo o nome do item a ser deletado
	                    boolean removido = listaDeItens.remove(itemDeletado); // tentando remover o item da lista
	                    if (removido) {
	                        System.out.println("Paciente Excluido com sucesso!");
	                    } else {
	                        System.out.println("O nome do Paciente não foi encontrado na lista.");
	                    }
	                    break;
	                
	                case 3:
	                    if (listaDeItens.isEmpty()) { // verificando se a lista está vazia
	                        System.out.println("A lista esta vazia.");
	                    } else {
	                        System.out.println("Lista do Pacientes cadastrados:");
	                        for (String item : listaDeItens) { // percorrendo a lista e imprimindo os itens
	                            System.out.println(item);
	                        }
	                    }
	                    break;
	                
	                case 4:
	                    System.out.println("Encerrando o programa...");
	                    break;
	                
	                default:
	                    System.out.println("Opção inválida! Tente novamente.");
	                    break;
	            }
	            
	            System.out.println(); // pulando uma linha antes de mostrar o menu novamente
	            
	        }
	        
	        scanner.close(); // fechando o objeto Scanner

	}

}
