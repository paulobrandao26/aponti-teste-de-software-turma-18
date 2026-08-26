
# Atividade Avaliativa — Heurísticas de Teste

**Projeto:** Clínica Psi — Time 2
**Módulo:** Funcionários
**Funcionalidade analisada:** Tela "Novo registro — Funcionários" (cadastro de funcionário)

---

## Heurísticas escolhidas

1. **Heurística de Nielsen — Prevenção de erros** ("Error Prevention")
2. **Testing Tour — "Landmark Tour"** (James Whittaker), que percorre
   sistematicamente cada campo, botão e elemento visível da tela, verificando
   se cada um se comporta como esperado antes de avançar no fluxo.

### Justificativa das escolhas

- **Prevenção de erros (Nielsen)** foi escolhida porque esta é uma tela de
  cadastro com campos livres (nome, cargo, telefone, e-mail) sem nenhuma
  indicação visual de formato esperado, campo obrigatório ou máscara de
  digitação. Essa heurística direciona a análise para onde o sistema deveria
  impedir a entrada de dados inválidos antes mesmo do envio, e não apenas
  reagir com uma mensagem de erro depois.
- **Landmark Tour** foi escolhida porque a tela tem poucos elementos (4 campos
  + 2 botões), o que torna viável e eficaz percorrer cada um individualmente,
  testando limites, formatos e comportamento isolado — sem precisar de um
  roteiro de navegação mais amplo.

---

## Aplicação na funcionalidade: Novo registro — Funcionários

### Falhas identificadas

| # | Falha | Onde ocorre |
|---|---|---|
| 1 | Nenhum campo indica visualmente se é obrigatório (sem asterisco ou marcação) | Todos os 4 campos do formulário |
| 2 | Campo "Telefone" não possui máscara nem validação de formato aparente | Campo Telefone |
| 3 | Campo "E-mail" não possui validação de formato (ex.: exigir "@" e domínio) visível na interface | Campo E-mail |
| 4 | Não há indicação de limite de caracteres em "Nome completo" e "Cargo" | Campos Nome completo e Cargo |
| 5 | Botão "Salvar registro" não apresenta estado de carregamento/feedback visual ao ser clicado | Botão Salvar registro |

### Riscos identificados

- **Cadastro de funcionário com dados incompletos ou inválidos**: sem
  indicação de obrigatoriedade, um usuário pode salvar um registro sem
  telefone ou e-mail, gerando dados incompletos no sistema que podem
  atrapalhar comunicação futura com o funcionário.
- **Telefone e e-mail em formato inconsistente**: sem máscara ou validação,
  diferentes funcionários podem ser cadastrados com formatos diferentes de
  telefone (com/sem DDD, com/sem traço) e e-mails digitados incorretamente,
  dificultando buscas, filtros e integrações futuras (ex.: envio de
  notificação).
- **Duplo clique / duplo envio**: sem feedback visual de carregamento no botão
  "Salvar registro", existe o risco de o usuário clicar mais de uma vez
  pensando que o clique não funcionou, criando registros duplicados do mesmo
  funcionário.
- **Perda de dados ao clicar em "Cancelar" por engano**: como os dois botões
  ficam próximos e com pesos visuais parecidos, existe risco de o usuário
  cancelar um cadastro já preenchido por engano, sem nenhuma confirmação
  antes.

### Áreas que merecem mais atenção

- **Validação de formato nos campos de contato (telefone e e-mail)**: são os
  dois campos mais propensos a erro de digitação e mais importantes para a
  comunicação com o funcionário — merecem prioridade de tratamento.
- **Feedback visual de ações (salvar/cancelar)**: o sistema precisa deixar
  claro quando uma ação está em andamento e confirmar antes de descartar
  dados preenchidos.
- **Indicação clara de campos obrigatórios**: previne que o registro seja
  salvo incompleto, reduzindo a necessidade de correção posterior.

---

## Conclusão

A combinação da heurística de **Prevenção de Erros** com o **Landmark Tour**
foi eficaz para revelar riscos de qualidade de dados na tela de cadastro de
Funcionários — especialmente relacionados à ausência de validação de formato
e de feedback visual, que podem levar a registros incompletos, inconsistentes
ou duplicados no sistema da Clínica Psi.
