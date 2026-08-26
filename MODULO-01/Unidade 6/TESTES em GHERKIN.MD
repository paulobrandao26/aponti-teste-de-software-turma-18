from pathlib import Path

conteudo = """# Atividade Avaliativa — BDD com Gherkin

## Funcionalidade: Cadastro de Funcionário

**Como** administradora do sistema  
**Eu quero** cadastrar um novo funcionário  
**Para que** ele possa acessar o sistema e realizar seu trabalho

### Cenário 1: Cadastro de funcionário com dados válidos

**Dado** que a administradora está na tela de cadastro de funcionário  
**Quando** ela preenche todos os campos obrigatórios com dados válidos  
**E** confirma o cadastro  
**Então** o funcionário deve ser cadastrado com sucesso  
**Mas** o sistema deve exibir uma mensagem de confirmação

### Cenário 2: Tentativa de cadastro com e-mail já existente

**Dado** que a administradora está na tela de cadastro de funcionário  
**Quando** ela preenche os dados com um e-mail já cadastrado no sistema  
**E** confirma o cadastro  
**Então** o sistema deve exibir uma mensagem de erro informando que o e-mail já está em uso  
**Mas** o cadastro não deve ser salvo no banco de dados
"""

caminho = Path("/mnt/data/atividade_bdd_cadastro_funcionario.md")
caminho.write_text(conteudo, encoding="utf-8")
print(f"Arquivo criado: {caminho}")
