# Plano de Testes

Projeto: sistema bancario ficticio (login, saldo, transferencias, extrato).

## 1. Escopo de testes

Inclui: login, exibicao de saldo, transferencias e extrato.
Nao inclui: funcionalidades secundarias ainda nao finalizadas, como notificacoes ou personalizacao de tema.

## 2. Tipos de teste aplicados

Funcional, regressao e smoke test, com apoio de testes exploratorios e de usabilidade nas telas principais. Performance fica fora do escopo deste ciclo, sendo tratada proximo ao lancamento.

## 3. Criterios de entrada e saida

Entrada: funcionalidade implementada e disponivel em ambiente de testes, sem erros bloqueantes conhecidos.
Saida: casos de teste criticos executados com sucesso, sem defeitos de alta severidade em aberto e smoke test aprovado na ultima versao.

## 4. Ambiente de testes

Ambiente de homologacao, separado do ambiente de producao, com massa de dados fictícia representando cenarios reais de uso.

## 5. Recursos e responsabilidades

2 pessoas responsaveis pelos testes. Uma foca em testes funcionais e de regressao, outra em testes exploratorios e de usabilidade. Desenvolvedores apoiam na correcao dos defeitos identificados.

## 6. Cronograma basico

Smoke test a cada entrega. Testes funcionais e de regressao ao longo do desenvolvimento. Testes exploratorios e de usabilidade concentrados perto dos marcos principais do projeto. Ciclo final de testes antes do prazo de entrega.

## 7. Riscos e contingencias

Risco: prazo apertado pode reduzir o tempo de testes.
Contingencia: priorizar funcionalidades criticas e automatizar testes repetitivos para ganhar tempo.

Risco: time reduzido pode gerar sobrecarga.
Contingencia: focar esforco manual apenas onde ha maior risco, deixando o restante para automacao ou ciclos posteriores.
