# Caso de Teste Tradicional x BDD

## Caso de Teste Tradicional: Login com credenciais válidas

**ID:** FUN001
**Ator:** Funcionário da clínica
**Objetivo:** Validar o login de um funcionário utilizando credenciais válidas.

### Pré-condição

O funcionário deve estar cadastrado no sistema e estar na tela de login.

### Dados de teste

* **E-mail:** `brunosss@gmail.com`
* **Senha:** `12345678`

### Passos

| Passo | Ação                                   | Resultado esperado                                                                                |
| ----: | -------------------------------------- | ------------------------------------------------------------------------------------------------- |
|     1 | Acessar a tela de login                | A tela de login deve ser exibida.                                                                 |
|     2 | Informar o e-mail `brunosss@gmail.com` | O e-mail deve ser preenchido no campo.                                                            |
|     3 | Informar a senha `12345678`            | A senha deve ser preenchida no campo.                                                             |
|     4 | Clicar no botão **"Entrar"**           | O sistema deve validar as credenciais.                                                            |
|     5 | Verificar o resultado do login         | O funcionário deve ser autenticado e redirecionado para a tela principal destinada ao seu perfil. |

### Resultado esperado

O funcionário deve realizar o login com sucesso e acessar a tela principal correspondente ao seu perfil.

---

# Comparação entre BDD e Teste Tradicional

## Qual formato é mais fácil de escrever?

O **BDD é mais fácil de escrever**, principalmente para cenários simples, pois utiliza uma estrutura objetiva: **Given, When e Then**. Isso permite descrever rapidamente o comportamento esperado do sistema.

## Qual comunica melhor o comportamento?

O **BDD comunica melhor o comportamento do sistema**, pois descreve de forma clara o que deve acontecer a partir de uma determinada situação. Além disso, sua estrutura facilita o entendimento tanto por pessoas técnicas quanto por pessoas não técnicas.

## Qual seria mais fácil de manter?

O **BDD tende a ser mais fácil de manter**, pois descreve o comportamento esperado sem detalhar excessivamente os passos de execução. Se a interface do sistema mudar, por exemplo, o cenário BDD pode continuar válido, enquanto um teste tradicional pode precisar de alterações em vários passos.

## Conclusão

Para este caso, o **BDD é mais simples de escrever, comunica melhor a regra de negócio e tende a ser mais fácil de manter**.

Já o **teste tradicional** é mais detalhado e pode ser mais adequado quando é necessário documentar exatamente os passos que o testador deve executar e os resultados esperados em cada etapa.
