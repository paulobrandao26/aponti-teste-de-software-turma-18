# Testes BDD — Cadastro de Funcionário

**Projeto:** Clínica Psi — Time 2
**Módulo:** Gestão da Clínica → Funcionários

---

## Funcionalidade: Cadastro de funcionário na Clínica Psi

> **Como** administrador do sistema da clínica
> **Eu quero** cadastrar novos funcionários
> **Para que** eles fiquem registrados no sistema e possam ser vinculados às suas atividades na clínica

### Contexto

\`\`\`gherkin
Dado que estou logado como administrador no sistema
E estou na tela "Novo registro — Funcionários"
\`\`\`

---

## Cenário 1: Cadastrar funcionário com todos os campos preenchidos corretamente (caminho feliz)

\`\`\`gherkin
Dado que preencho o campo "Nome completo" com "Mariana Souza Lima"
E preencho o campo "Cargo" com "Recepcionista"
E preencho o campo "Telefone" com "(81) 98765-4321"
E preencho o campo "E-mail" com "mariana.souza@clinicapsi.com"
Quando clico no botão "Salvar registro"
Então o sistema deve validar todos os campos com sucesso
E o funcionário deve ser salvo na base de dados
E devo ser redirecionado para a listagem de funcionários
E o novo funcionário "Mariana Souza Lima" deve aparecer na lista
\`\`\`

---

## Cenário 2: Tentar salvar registro com o campo "Nome completo" em branco (caminho alternativo)

\`\`\`gherkin
Dado que deixo o campo "Nome completo" em branco
E preencho o campo "Cargo" com "Recepcionista"
E preencho o campo "Telefone" com "(81) 98765-4321"
E preencho o campo "E-mail" com "carlos.santos@clinicapsi.com"
Quando clico no botão "Salvar registro"
Mas o sistema identifica que o campo obrigatório "Nome completo" não foi preenchido
Então o registro não deve ser salvo
E devo visualizar uma mensagem de erro indicando que o campo "Nome completo" é obrigatório
E devo permanecer na tela "Novo registro — Funcionários"
E os demais campos preenchidos devem ser mantidos
\`\`\`

---

## Resumo dos cenários

| Cenário | Tipo | Resultado esperado |
|---|---|---|
| 1 — Cadastro com dados válidos | Caminho feliz | Funcionário salvo com sucesso |
| 2 — Nome completo em branco | Caminho alternativo (Mas) | Erro de validação, registro não salvo |
