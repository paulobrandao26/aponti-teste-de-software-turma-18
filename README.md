# 📚 APONTI - Formação em Testes de Software
👋 Bem-vindo!
Este repositório reúne materiais utilizados na Formação em Testes de Software,
organizados em trilhas de aprendizagem.
## 🎯 Objetivos
- 🏆 Construir um portfólio profissional
---
# 🛤️Trilhas
|**Módulo** | **Conteúdo** |
|---------|----------|
| 01 | 🌿 *Git e GitHub* |
| 02 | 🧠 *Lógica básica de sistemas* |
| 03 | 🧪 *Testes manuais* |
| 04 | 🛠️ *Ferramentas básicas da área* |
| 05 | 🔌 *Testes de API* |
| 06 | 🤖 *Automação de testes* |
| 07 | 🚀 *Qualidade de software e integração contínua* |
---

Comandos Git

bash# Verificar status do repositório
git status

# Adicionar arquivos ao staging
git add .

# Criar um commit
git commit -m "feat: adiciona exercícios da trilha 01"

# Enviar para o repositório remoto
git push origin main

# Atualizar repositório local
git pull origin main

# Ver histórico de commits
git log --oneline

Comandos do Terminal

bash# Criar uma pasta
mkdir nome-da-pasta

# Criar um arquivo
touch nome-do-arquivo.md

# Listar arquivos (incluindo ocultos)
ls -la

# Navegar entre pastas
cd nome-da-pasta

# Voltar uma pasta
cd ..

# Ver conteúdo de um arquivo
cat README.md

Código em Python

python# Exemplo de script de automação simples
def verificar_status(teste: str, passou: bool) -> str:
    if passou:
        return f"✅ PASSOU: {teste}"
    else:
        return f"❌ FALHOU: {teste}"

testes = [
    ("Login com credenciais válidas", True),
    ("Login com senha errada", True),
    ("Cadastro com e-mail duplicado", False),
]

for nome, resultado in testes:
    print(verificar_status(nome, resultado))



## 📖 Como utilizar
**Cada pasta representa um módulo do curso.
Dentro de cada módulo você encontrará:**
- 📄 *Slides*
- 📚 *Tutoriais*
- ✍️ *Exercícios*
- 💻 *Projetos*
- 🎯 *Desafios*
- 📑 *Leituras complementares*
---
## 💼 Projetos

**Portifolio:** https://paulobrandao26.github.io/portifolio-FrontEnd/

---
## 📜 Licença



