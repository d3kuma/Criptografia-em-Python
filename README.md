# Criptografia em Python

Minha primeira criptografia em python, baseada em RSA.

**Cálculos para realizar a criptografia em RSA**

Começamos com a escolha da chave pública, cáculada a partir de dois números primos denominaodps no código da criptogrfia  P e Q, o correto e que eles sejam aleatórios, mas no algoritomo foram escolhidos. Motivo e que após a escolha precisamos achar o E sendo MDC igual a 1. e superior a  255, caso contrario cifra não funconaria. Exemplo de como foi realiado a cifra:

```P = 41 e Q = 107```

Após a escolha dos números primos, precisamos achar N, vai ser a multiplicação de P e Q:

```N = P X Q```

```N = 4387```

Agora o E pode ser escolhido de forma aleatória, mas o seu  MDC deve ser igual a 1:

```E = 3```

```MDC(E, N) = 1```

Por fim, precisaremos também de D. Mesmo vai ser localizado da seguinte forma E X D  Quando dividido  por  (P -1) X (Q -1), vai precisar dar resto 1. Para facilitar essa conta utilizamos um enquanto E X D mod M != 1, D recebe +1.
Informamos que M vai receber (P -1) X (Q -1), então:

```E X D = 1 mod(M)```

A = caractere digitado pelo usuário, vai ser convertido para a tabela ASCI.

Para cifrar faremos a seguinte conta:

```Cifra = (A ^ E) mod N```

E decifrar:

```Descrip = (Cifra ^ D) mod N```
