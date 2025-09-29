# Experimento 3: Deletando Tarefas

## 3.2) O que aconteceu?
O programa cria 2 task onde a primeira tem a função de piscar um LED indefinidamente. Enquanto a segunda é um contador, onde quando chega em 20, deleta a task 1, parando assim de piscar o LED.

## 3.3) Altere o código para que a task2 conte até 25 por exemplo e seja deletada?

adicionado o seguinte codigo para o programa:

```bash
if(count>=25) /*se maior ou igual a 25*/
    {
      
      Serial.println("Task 2 Deletada!"); /*Mensagem na serial*/
      vTaskDelete(xTask2Handle);          /*Deleta task 2*/         
    }
```

## 3.4) O que aconteceu?
Ao chegar em 20 a task1 finaliza e o LED para de piscar; ao chegar em 25 a task2 finaliza e para qualquer interação do programa. 