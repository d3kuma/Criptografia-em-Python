# Criptografia em Python

Minha primeira criptografia em python, baseada em calculos RSA.

Cálculo para realizar a criptografia em RSA.

Começamos com a escolha da chave pública, cáculada a partir de dois números primos denominaodps no código da criptogrfia  P e Q, o correto e que eles sejam aleatórios, mas no algoritomo foram escolhidos. Motivo e que após a escolha precisamos achar o E sendo MDC igual a 1. e superior a  255, pois convertemos os caracteres para a tabela ASCII. Colocarei exemplo logo abaixo:

P = 41 e Q = 107

após a escolha dos números primos, precisamos achar N que vai ser a multiplicação de P e Q:

N = P X Q
N = 4387

Agora o E, ele pode ser escolhido de forma aleatória, mas o seu  MDC deve ser igual a 1:

E = 3
MDC(E, N) = 1

Por fim, D vai ser localizado. E X D  Quando Dividido  por  (P -1) X (Q -1), vai precisar dar resto 1.
Para facilitar  M vai receber (P -1) X (Q -1):

E X D = 1 mod(M)
Para facilitar essa conta utilizamos um enquanto E X D mod M != 1, D recebe +1

A = caractere digitado pelo usuário converto ele para a tabela ASCI

Cifra = (A ^ E) mod N

Para descifrar fazemos:

Descrip = (Cifra ^ D) mod D

