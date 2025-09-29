 programa {
  funcao modulo1() {
    inteiro tentativas = 0
    cadeia senhaCorreta = "1234"
    cadeia senhaDigitada

    enquanto(tentativas < 3){
      escreva("digite sua senha de 4 Digitos:")
      leia(senhaDigitada)

      se (senhaCorreta == senhaDigitada){
        escreva("Acesso permitido")
        pare
      } senao {
        tentativas = tentativas + 1
        escreva("Senha incorreta. Tentativa ", tentativas, " de 3.\n")
      }
    }
    se (tentativas == 3){
      escreva("Conta bloqueada por excesso de tentativas")
    }
  }

  funcao modulo2() {
    cadeia senha
    cadeia fracas[3] = {"123","admin","senha", "4321", "1111", "2222"}
    inteiro i, fraca = 0

    escreva("digite uma nova senha: ")
    leia(senha)
    para(i = 0; i < 3; i++){
      se(senha == fracas[i]){
        fraca = 1
      }
    }
    se(fraca == 1){
      escreva("senha fraca")
    } senao {
      escreva("senha forte")
    }
  }

  funcao modulo3() {
    inteiro falhas = 0
    inteiro limite = 5
    inteiro i

    para(i = 1; i <= 10; i++){
      escreva("Tentativa ", i, ": falhou! \n")
      falhas = falhas + 1

      se(falhas >= limite){
        escreva("ALERTA: Possivel ataque hacker! \n")
        pare
      }
    }
  }

  funcao inicio() {
    escreva("----- Módulo 1: Verificacao de senha (até 3 tentativas) -----\n")
    modulo1()

    escreva("\n----- Módulo 2: Verificacao de senhas fracas -----\n")
    modulo2()

    escreva("\n----- Módulo 3: Contador de falhas e alerta -----\n")
    modulo3()
   
  }
}

 
