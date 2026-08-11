# Caso de Teste BDD — Login de Funcionário

## 1. Quem é o ator?

**Funcionário da clínica**

## 2. Qual é o estado inicial?

O funcionário está na **tela de login** do sistema.

```gherkin
Feature: Login de funcionário

  Scenario: Funcionário realiza login com credenciais válidas
    Given que o funcionário está na tela de login
    When ele informa um e-mail cadastrado
    And informa a senha correspondente
    And clica no botão "Entrar"
    Then o sistema deve autenticar o funcionário
    And deve redirecioná-lo para a tela de administrador
```

## 3. Qual ação realmente importa?

**Informar credenciais válidas e clicar no botão "Entrar".**

## 4. O resultado é observável?

**Sim.** O resultado é observável quando o funcionário consegue realizar o login com sucesso e acessar a **tela principal destinada a ele**.
