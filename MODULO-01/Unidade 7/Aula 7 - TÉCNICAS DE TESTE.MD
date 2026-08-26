# Atividade Avaliativa — Casos de Teste (Valor Limite, Particionamento de Equivalência e Transição de Estados)

**Projeto:** Clínica Psi — Time 2
**Módulo:** Funcionários
**Funcionalidade analisada:** Tela "Novo registro — Funcionários"

**Regras de negócio assumidas para os campos** (pela ausência de regras explícitas
visíveis na tela, foram definidas regras razoáveis para viabilizar os testes):
- **Nome completo**: obrigatório, mínimo 3 e máximo 100 caracteres
- **Cargo**: obrigatório, mínimo 2 e máximo 50 caracteres
- **Telefone**: obrigatório, deve conter entre 10 e 11 dígitos numéricos
- **E-mail**: obrigatório, deve conter formato válido (`texto@dominio.com`)

---

## Casos de Valor Limite (Boundary Value Analysis)

| # | Entrada | Técnica utilizada | Resultado esperado |
|---|---|---|---|
| VL1 | Telefone com **9 dígitos** (`987654321`) | Valor limite — abaixo do mínimo (10) | Sistema deve rejeitar e exibir mensagem de telefone inválido |
| VL2 | Telefone com **10 dígitos** (`8112345678`) | Valor limite — exatamente no mínimo aceito | Sistema deve aceitar e salvar o registro normalmente |
| VL3 | Nome completo com **101 caracteres** | Valor limite — acima do máximo (100) | Sistema deve rejeitar e exibir mensagem de limite de caracteres excedido |

---

## Casos de Particionamento de Equivalência (Equivalence Partitioning)

| # | Entrada | Técnica utilizada | Resultado esperado |
|---|---|---|---|
| PE1 | E-mail válido (`ana.souza@clinicapsi.com`) | Partição válida — formato de e-mail correto | Sistema deve aceitar e salvar o registro normalmente |
| PE2 | E-mail sem "@" (`anasouzaclinicapsi.com`) | Partição inválida — formato de e-mail incorreto | Sistema deve rejeitar e exibir mensagem de e-mail inválido |
| PE3 | Campo "Cargo" vazio (não preenchido) | Partição inválida — campo obrigatório ausente | Sistema deve rejeitar o envio e sinalizar o campo obrigatório |

---

## Estados e Transições (State Transition Testing)

### Estados identificados

1. **Rascunho** — formulário aberto, com ou sem dados parcialmente preenchidos, ainda não salvo
2. **Ativo** — funcionário cadastrado com sucesso e salvo no sistema
3. **Cancelado/Descartado** — formulário fechado via botão "Cancelar" antes de salvar

### Transições testadas

| # | Transição | Entrada / ação | Resultado esperado |
|---|---|---|---|
| ET1 | Rascunho → Ativo | Preencher todos os campos corretamente e clicar em "Salvar registro" | O funcionário passa para o estado Ativo e aparece na listagem de Funcionários |
| ET2 | Rascunho → Cancelado | Preencher parcialmente os campos e clicar em "Cancelar" | O formulário é descartado, nenhum registro é criado, sistema retorna à listagem |
| ET3 | Rascunho → Rascunho (permanece) | Clicar em "Salvar registro" com campos obrigatórios vazios/inválidos | O sistema permanece na tela de cadastro (não transiciona para Ativo), exibindo mensagem de erro |

---

## Resumo

| Técnica | Quantidade de casos |
|---|---|
| Valor Limite | 3 |
| Particionamento de Equivalência | 3 |
| Estados e Transições | 3 |

Essas técnicas, combinadas, cobrem tanto os limites numéricos de entrada (valor
limite), quanto as categorias de dados válidos/inválidos (particionamento), quanto
o comportamento do fluxo de cadastro como um todo (transição de estados),
oferecendo uma cobertura mais ampla da funcionalidade de cadastro de
Funcionários do que qualquer técnica isolada.
