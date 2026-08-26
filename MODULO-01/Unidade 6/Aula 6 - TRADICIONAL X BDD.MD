

"""# Atividade Avaliativa — BDD x Tradicional

## Funcionalidade: Cadastro de Agendamento

### 1. Abordagem BDD

**Como** administradora do sistema  
**Eu quero** cadastrar um novo agendamento  
**Para que** uma consulta seja registrada na agenda da clínica

#### Cenário 1: Cadastro de agendamento com dados válidos

**Dado** que a administradora está na tela de cadastro de agendamento  
**Quando** ela preenche paciente, psicólogo, data, horário e status com dados válidos  
**E** confirma o cadastro  
**Então** o agendamento deve ser cadastrado com sucesso  
**Mas** o sistema deve exibir uma mensagem de confirmação

#### Cenário 2: Tentativa de cadastro de agendamento sem preencher campo obrigatório

**Dado** que a administradora está na tela de cadastro de agendamento  
**Quando** ela deixa um campo obrigatório sem preenchimento  
**E** confirma o cadastro  
**Então** o sistema deve impedir o cadastro  
**Mas** deve exibir uma mensagem informando que o campo é obrigatório

---

## 2. Abordagem Tradicional

### Caso de teste 1 — Cadastro de agendamento com dados válidos

**Passos:**

1. Acessar a tela de cadastro de agendamento.
2. Preencher o campo Paciente.
3. Preencher o campo Psicólogo.
4. Informar uma data válida.
5. Informar um horário válido.
6. Informar o status.
7. Clicar em **Salvar registro**.

**Resultado esperado:**  
O agendamento deve ser cadastrado com sucesso e o sistema deve exibir uma mensagem de confirmação.

### Caso de teste 2 — Cadastro sem preencher campo obrigatório

**Passos:**

1. Acessar a tela de cadastro de agendamento.
2. Preencher os campos obrigatórios, deixando um deles vazio.
3. Clicar em **Salvar registro**.

**Resultado esperado:**  
O sistema deve impedir o cadastro e exibir uma mensagem informando que o campo obrigatório precisa ser preenchido.

---

## 3. Comparação entre as abordagens

### Qual formato é mais fácil de escrever?

O formato tradicional é mais fácil de escrever, pois apresenta os passos de forma direta e objetiva.

### Qual comunica melhor o comportamento?

O BDD comunica melhor o comportamento, pois utiliza uma linguagem próxima à linguagem de negócio e descreve claramente o que deve acontecer em cada cenário.

### Qual seria mais fácil de manter?

O BDD seria mais fácil de manter, pois os cenários são organizados de forma clara e podem ser alterados conforme as regras do sistema mudam.
"""
