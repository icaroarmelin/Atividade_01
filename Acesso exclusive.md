# Acesso exclusivoCategoria: Crypto
Autor: professores

## Introdução

Desafio básico sobre cybersecurity(nesse caso sobre crypto) feito pelos professores como exemplo da aula sobre CTF. Esse desafio, para mim como iniciante, foi complicado por alguns motivos como por falta de conhecimento. Não tinha noção por exemplo que “XOR” seria “OU” em português, assim a dica seria o principal para dar o próximo passo. 


## Análise 
Dica / enunciado:


*"A lógica do algoritmo invasor é simples: 'ou é uma coisa, ou é outra, mas nunca as duas'. Use esse conhecimento contra a própria cifra para quebrar a criptografia.
Modelo de flag: FLAG{...}”*


Esse era o enunciado juntamente com um arquivo.txt que dentro tinha um código


“25783566184c44533c5f47583c464742534247533c5945151649”


Interpretação


Após a descoberta que precisaria usar o XOR pesquisei como ele realmente funciona, assim, entendi que ele analise bit por bit, verificando os 0s e 1s dos números em binário e que na cifra XOR:
C=P⊕K
C: texto cifrado
P: texto original
K: chave
Mas também pode ser desfeito fazendo o contrário:


K=C⊕P		e		P=C⊕K






Então após a divisão do código em hexadecimal, consegui pegar o binário de cada letra / número, assim, meu pensamento foi pegar a primeira parte da flag, que era “FLAG{“ e transformá-la com XOR, para obter um tradutor chave, que eu usaria para decifrar a cifra completa, usei o site dCode para fazer isso mas, fazendo na mão ficaria:


25 comparando-o com o o hexadecimal de f, que é 46 me dá a letra c, e aqui entra a comparação em binário: 25 = 0010 0101 e 46 = 0100 0110, sendo assim, iguais dão 0 e diferentes dão 1, ficando com o binário de 0110 0011, que convertendo para hexadecimal é 63 que em ASCII, me dá a letra c.


Resolução
fazendo isso com os primeiros hexadecimal do código e com a “FLAG{“, obtive a chave de “c4t!c”. 


 
Para decifrar a cifra, não sabia se o segundo ‘c’ era uma repetição ou fazia parte da chave, então após usar como parte da chave para decifrar dava erro.


kjyt4x\


Então decidi que era um caractere de repetição e retirei-o da chave, ficando “c4t!” que rodando mais uma vez o dCode me deu a flag: 



Conclusão
Esse foi meu primeiro desafio com cybersecurity, foi complicado no começo por não saber de várias coisas, mas depois que descobre a parte essencial, fica fácil continuar.
Um desafio legal que me fez aprender principalmente a usar ferramentas que estão ao nosso dispor como o dCode que foi essencial para resolução do problema e sobre a cifra XOR.
****
