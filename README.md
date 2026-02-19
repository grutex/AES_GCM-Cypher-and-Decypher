Para Criptografar uma mensagem:
--------------------
Plain Text e Key estão pre-setados no programa, mas podem ser alterados.

1 - crie um executável do código usando GCC ou qualquer outro compilador, passando -lssl e -lcrypto.
	ex.: gcc < programa.c > -o < nome_do_executavel > -lssl -lcrypto

2 - execute-o no terminal, um print com o exto cifrado, iv e a tag serão gerados baseados no plain_text
	e na chave.

3 - parâmetros criptografados, já em hexadecimal, serão gerados e imprimidos no terminal.




Para Descriptografar a mensagem:
-----------------------
1 - crie um executável do código usando GCC ou qualquer outro compilador, passando -lssl e -lcrypto.
	ex.: gcc < programa.c > -o < nome_do_executavel > -lssl -lcrypto

2 - passe na linha de comando o texto cifrado, o vetor de inicialização(iv) e a tag do GCM (em HEXADECIMAL)
	exatamente nessa ordem (argv[1], [2], [3]) valores que são dados após a execução do código.
	ex.: ./decrypt < hex_plaintext > <hex_iv> <hex_tagGCM>
		
3 - Se os parâmetros derem match, a mensagem pré-setada será printada no terminal.
