# Caso de Teste Alternativo BDD — Login de Funcionário

## 1. Quem é o ator?

**Funcionário da clínica**

## 2. Qual é o estado inicial?

O funcionário está na **tela de login** do sistema.

```gherkin
Feature: Login de funcionário

  Scenario: Funcionário tenta realizar login com credenciais inválidas
    Given que o funcionário está na tela de login
    When ele informa credenciais inválidas
    And clica no botão "Entrar"
    Then o sistema não deve autenticar o funcionário
    And deve exibir uma mensagem de erro
```

## 3. Qual ação realmente importa?

**Informar credenciais inválidas e clicar no botão "Entrar".**

## 4. O resultado é observável?

**Sim.** O resultado é observável quando o funcionário tenta realizar o login e o sistema **exibe uma mensagem de erro**, informando que as credenciais são inválidas.
