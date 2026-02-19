🛡️ AES-GCM Encryption/Decryption Tool
A simple implementation using OpenSSL to encrypt and decrypt messages with AES-GCM.

🇧🇷 Português (PT-BR)
🔐 Como Encriptar
O Plain Text (texto puro) e a Key (chave) estão pré-configurados no código, mas podem ser alterados livremente.

Compile o código: Utilize o GCC (ou outro compilador) passando as flags do OpenSSL.

Bash
gcc programa.c -o encrypt -lssl -lcrypto
Execute o programa: No terminal, rode o executável.

Bash
./encrypt
Resultado: O texto cifrado, o IV e a Tag serão gerados em formato hexadecimal e exibidos no console.

🔓 Como Decifrar
Compile o código:

Bash
gcc decifrar.c -o decrypt -lssl -lcrypto
Passe os parâmetros: Execute o programa enviando o texto cifrado, o IV e a Tag GCM (em hexadecimal) via linha de comando, exatamente nesta ordem:

Bash
./decrypt <hex_ciphertext> <hex_iv> <hex_tagGCM>
Sucesso: Se os parâmetros forem válidos e a tag coincidir, a mensagem original será revelada.

🇺🇸 English (EN-US)
🔐 How to Encrypt
Plain Text and Key are preset in the program but can be modified.

Compile the code: Use GCC or any other compiler, passing the -lssl and -lcrypto flags.

Bash
gcc program.c -o encrypt -lssl -lcrypto
Run the program: Execute it in your terminal.

Bash
./encrypt
Output: The ciphertext, IV, and Tag (in hexadecimal) will be generated and printed to the terminal.

🔓 How to Decrypt
Compile the code:

Bash
gcc decrypt.c -o decrypt -lssl -lcrypto
Provide parameters: Pass the ciphertext, Initialization Vector (IV), and the GCM tag (in HEX) via command line in this exact order (argv[1], [2], [3]):

Bash
./decrypt <hex_ciphertext> <hex_iv> <hex_tagGCM>
Success: If the parameters match, the original message will be decrypted and displayed.
