

                                Estruturando Casos de Teste



Caso 1
ID – G001
Título – Validar login com credenciais válidas
Pré-condições – Ter um usuário cadastrado no sistema.
Passos – P1 - Informar usuário válido; P2 - Informar senha válida; P3 - Clicar no botão Entrar
Resultado esperado – O sistema autentica o usuário e permite o acesso à conta.

Caso 2
ID – G002
Título – Validar login com senha incorreta
Pré-condições – Ter um usuário cadastrado no sistema.
Passos – P1 - Informar usuário válido; P2 - Informar senha incorreta; P3 - Clicar no botão Entrar
Resultado esperado – O sistema exibe mensagem de erro e não permite o acesso.

Caso 3
ID – G003
Título – Validar login com usuário inexistente
Pré-condições – Nenhuma.
Passos – P1 - Informar usuário não cadastrado; P2 - Informar qualquer senha; P3 - Clicar no botão Entrar
Resultado esperado – O sistema exibe mensagem de erro e não permite o acesso.

Caso 4
ID – G004
Título – Validar campo de usuário vazio
Pré-condições – Nenhuma.
Passos – P1 - Deixar o campo de usuário em branco; P2 - Informar senha válida; P3 - Clicar no botão Entrar
Resultado esperado – O sistema exibe mensagem informando que o campo é obrigatório.

Caso 5
ID – G005
Título – Validar campo de senha vazio
Pré-condições – Ter um usuário cadastrado no sistema.
Passos – P1 - Informar usuário válido; P2 - Deixar o campo de senha em branco; P3 - Clicar no botão Entrar
Resultado esperado – O sistema exibe mensagem informando que o campo é obrigatório.

Caso 6
ID – G006
Título – Validar bloqueio após múltiplas tentativas inválidas
Pré-condições – Ter um usuário cadastrado no sistema.
Passos – P1 - Informar usuário válido; P2 - Informar senha incorreta repetidamente até o limite permitido; P3 - Tentar logar novamente com a senha correta
Resultado esperado – O sistema bloqueia o acesso temporariamente, mesmo com a senha correta.

Caso 7
ID – G007
Título – Validar sensibilidade a maiúsculas e minúsculas na senha
Pré-condições – Ter um usuário cadastrado com senha contendo letras maiúsculas e minúsculas.
Passos – P1 - Informar usuário válido; P2 - Informar a senha correta trocando maiúsculas por minúsculas; P3 - Clicar no botão Entrar
Resultado esperado – O sistema rejeita o login por considerar a senha incorreta.

Caso 8
ID – G008
Título – Validar login colando usuário com espaços extras
Pré-condições – Ter um usuário cadastrado no sistema.
Passos – P1 - Colar o usuário válido com espaços em branco antes e depois; P2 - Informar senha válida; P3 - Clicar no botão Entrar
Resultado esperado – O sistema remove os espaços extras e autentica o usuário normalmente.

Caso 9
ID – G009
Título – Validar exibição da senha ao clicar no ícone "mostrar senha"
Pré-condições – Estar na tela de login.
Passos – P1 - Digitar uma senha; P2 - Clicar no ícone de mostrar senha
Resultado esperado – A senha passa a ser exibida em texto legível.

Caso 10
ID – G010
Título – Validar login pressionando "Enter" ao invés de clicar no botão
Pré-condições – Ter um usuário cadastrado no sistema.
Passos – P1 - Informar usuário válido; P2 - Informar senha válida; P3 - Pressionar a tecla Enter
Resultado esperado – O sistema autentica o usuário normalmente.
