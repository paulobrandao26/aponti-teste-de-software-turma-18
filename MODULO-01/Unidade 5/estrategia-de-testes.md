# Estrategia de Testes

Projeto: sistema bancario ficticio (login, saldo, transferencias, extrato), em desenvolvimento ativo, com prazo definido, time reduzido e uso por usuarios reais.

## 1. Objetivo da estrategia

Garantir a estabilidade das funcionalidades criticas (login, saldo e transferencias), ja que falhas nessas areas afetam a confianca do usuario e podem gerar prejuizo financeiro. Maior atencao para seguranca, integridade dos dados e usabilidade basica.

## 2. Tipos de teste prioritarios

Alta prioridade: funcional, regressao e smoke test.
Media prioridade: usabilidade e exploratorio.
Baixa prioridade: performance e compatibilidade entre dispositivos.

Justificativa: com time reduzido, o foco vai para os testes que reduzem o maior risco com menor esforco. Performance e compatibilidade ficam para uma fase posterior, mais proxima do lancamento.

## 3. Abordagens de teste

Manuais: testes exploratorios e de usabilidade, que dependem de julgamento humano.
Automatizados: regressao e smoke test das funcionalidades criticas, por serem repetitivos e frequentes.

Justificativa: automatizar o repetitivo libera o time reduzido para focar no que exige investigacao humana, sem tornar o processo lento demais para o prazo do projeto.

## 4. Riscos e mitigacao

Riscos: falha em transferencias ou saldo incorreto, vulnerabilidade no login, regressao causada por novas entregas, prazo apertado.

Mitigacao: testes funcionais e de regressao concentrados nas areas financeiras, automacao para validacao constante, testes exploratorios para cobrir o que os casos formais nao preveem, e smoke test a cada entrega para barrar versoes instaveis cedo.

## 5. Recursos e cronograma

2 pessoas dedicadas a testes, junto com os desenvolvedores.

Smoke test a cada entrega. Funcional e regressao de forma continua. Exploratorio e usabilidade concentrados em marcos do projeto. Performance concentrado proximo ao lancamento.
