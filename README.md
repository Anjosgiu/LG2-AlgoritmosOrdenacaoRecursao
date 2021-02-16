# LG2-AlgoritmosOrdenacaoRecursao

Aluna Giulia Santana dos Anjoa SP3025918

Algoritmos de ordenacao e recursao

//CODIGO AULA 1 - Bubble Sort//
 public static void main(String[] args){
 
  int vetor[] = {3,6,2,1,8,4};
  int aux;
  boolean controle;
  
    for(int i=0; i< vetor.length; ++i){
      controle = true;
      for(int j= 0; j< (vetor.length -1) ++j){
      
        if(vetor[j] > vetor[j + 1]){
          aux = vetor[j];
          vetor[j] = vetor[j + 1];
          vetor[j + 1]; = aux;
          controle = false;
          }
        }
        if(controle){
          break;
          }
        }
}

//CODIGO AULA 2 - Selection Sort//

import java.util.Arrays;
import java.util.Random;

public class Principal{
  public static void man(String[] args){
    int []v = gerarVetor(20);
    selectionSport(v);
    System.out.println(Arrays.toString(v));
    }
    
    private static void selectionSort(int[] v) {
      for(int i = 0; i < v.length; i++){
        int menor = i;
        for(int j=i + 1; j < v.length; j++){
          if(v[j] < v[menor])
            menor = j;
        }
        trocar(v, i, menor);
      }
   }
    private static void trocar(int[] v, int i, int menor){
      int aux = v[i];
      v[i] = v[menor];
      v[menor] = aux;
   }
    public static int[] gerarVetor(int n){
      int[]v = new int[n];
      Random gerador = new Random();
      for (int i = 0; i < n; i++){
        v[i] = gerador.nextInt(100);
        }
        return v;
     }
}

//CODIGO AULA 3 - Recursividade//

public static int Somar (int num1, int num2){
  return num1 + num2;
}
public static int subtrair (int num1, int num2){
  return num1 - num2;
}
public static int multiplicar (int num1, num2){
  return num1 * num2;
}

public static int potencia (int num1, int num2){
  int total = 1;
  for (int i=1; i < num2; i++){
    total *= num1;
   }
   
   return total;
  }
  
  public static int fatoralNaoRecursivo(int num){
  
    if (num == 0){
    return 1;
   }
   
    int total = 1;
    for (int i=num; i>1; i--){
      total *= i;
    }
    return total;
    }
    
    
    //fatorial(5) = 5 * fatorial(4)
    //fatorial(4) = 4 * fatorial(3)
    //fatorial(3) = 3 * fatorial(2) 
    //fatorial(2) = 2 * fatorial(1)
    //fatorial(1) = 1 * fatorial(0)
    //fatorial(0) = 1;
    
    public static int fatorial(int num){
    
    if(num == 0){
      return 1;
    }
    return num * fatorial(num-1);
   }
  }
