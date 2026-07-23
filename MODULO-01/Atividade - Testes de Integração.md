# Testes de Integração

## 1 - Cadastro de paciente integrado ao banco de dados

**Componentes integrados:**  
Cadastro de paciente + Banco de dados

**Ação:**  
Cadastro de um novo paciente

**Resultado esperado:**  
Dados do paciente armazenados corretamente no banco de dados

**Risco:**  
Falha na gravação dos dados, impedindo o cadastro ou gerando informações inconsistentes


---

## 2 - Compra de produto integrada ao estoque

**Componentes integrados:**  
Compra de Produto + Estoque (Banco de dados)

**Ação:**  
Compra do produto e atualização da quantidade disponível no estoque

**Resultado esperado:**  
Compra realizada com sucesso e estoque atualizado corretamente

**Risco:**  
Falha na comunicação com o estoque, causando divergência na quantidade de produtos disponíveis


---

## 3 - Receita e despesa integradas ao relatório financeiro

**Componentes integrados:**  
Receitas e Despesas + Relatório Financeiro

**Ação:**  
O usuário cadastra uma receita e uma despesa

**Resultado esperado:**  
Informações de gastos e receitas são enviadas ao relatório financeiro e exibidas corretamente

**Risco:**  
O sistema não cadastrar ou não apresentar todas as informações inseridas pelo usuário, causando divergências no relatório financeiro


---

## 4 - Reagendamento integrado à liberação do horário anterior

**Componentes integrados:**  
Agendamento + Agenda

**Ação:**  
Usuário seleciona um novo horário disponível para o reagendamento da consulta

**Resultado esperado:**  
Novo horário é reservado e o horário anterior é liberado corretamente

**Risco:**  
Falha no processo de reagendamento, mantendo o horário antigo bloqueado ou causando conflito de horários


---

## 5 - Agendamento integrado à agenda do psicólogo

**Componentes integrados:**  
Agendamento + Agenda do psicólogo

**Ação:**  
Paciente escolhe um horário disponível para realizar a consulta com o psicólogo

**Resultado esperado:**  
Agendamento concluído com sucesso e horário registrado como ocupado na agenda do psicólogo

**Risco:**  
Falha na comunicação entre o agendamento e a agenda do psicólogo, permitindo conflitos ou perda de informações da consulta
