# Classificacao dos Cenarios de Teste - Manual ou Automatizado

Baseado nos cenarios de Smoke, Sanidade e Regressao definidos anteriormente para o sistema bancario ficticio.

## Smoke Test

1. Login com usuario e senha validos redireciona para tela inicial — **Automatizado**. Executado a cada entrega, alta repeticao e baixo custo de manutencao, ideal para automacao.
2. Tela inicial carrega sem erros apos o login — **Automatizado**. Verificacao simples e repetitiva, facil de automatizar.
3. Saldo e exibido na tela inicial — **Automatizado**. Checagem objetiva de presenca de elemento, boa candidata a automacao.
4. Sistema abre sem erro/crash — **Automatizado**. Teste basico e recorrente, executado em todo deploy.
5. Logout funciona e retorna a tela de login — **Automatizado**. Fluxo simples e estavel, com baixo custo de automacao.

Justificativa geral: smoke tests sao executados com alta frequencia (a cada deploy), o que torna a automacao mais vantajosa a medio prazo, mesmo com custo inicial de criacao dos scripts.

## Sanity Test

1. Login com senha incorreta exibe mensagem de erro — **Automatizado**. Cenario estavel e repetido a cada nova versao da correcao.
2. Login com usuario bloqueado ou inexistente e tratado corretamente — **Automatizado**. Regra de negocio bem definida, facil de validar via script.
3. Saldo exibido corresponde ao valor real da conta — **Manual**. Exige comparacao com dado externo (extrato ou banco), com maior valor de analise humana no primeiro ciclo apos a mudanca.
4. Saldo atualiza corretamente apos uma transacao — **Automatizado**. Fluxo repetitivo e criterio objetivo de validacao.
5. Formatacao do saldo esta correta — **Manual**. Envolve percepcao visual e detalhes de exibicao, mais eficiente revisar manualmente nesse momento pontual.

Justificativa geral: sanity test valida uma mudanca especifica, entao o equilibrio entre manual e automatizado depende da estabilidade do cenario. Regras de negocio claras favorecem automacao, enquanto validacoes visuais ou comparativas pontuais favorecem execucao manual.

## Regression Test

1. Transferencias continuam funcionando apos o ajuste no saldo — **Automatizado**. Fluxo critico, executado repetidamente a cada nova entrega.
2. Extrato continua exibindo o historico corretamente — **Automatizado**. Verificacao estruturada e recorrente, adequada para script.
3. Recuperacao de senha continua funcionando — **Automatizado**. Fluxo estavel e de alta repeticao ao longo do projeto.
4. Login via biometria ou token continua funcionando — **Manual**. Depende de hardware ou simulacao especifica, com maior custo e complexidade para automatizar nesta fase.
5. Outras telas com saldo permanecem consistentes com a tela inicial — **Manual**. Verificacao cruzada entre telas, mais viavel manualmente enquanto o numero de telas envolvidas for pequeno.

Justificativa geral: a regressao cobre fluxos essenciais que se repetem a cada nova versao, o que justifica a automacao na maior parte dos casos. Cenarios que dependem de hardware, integracao externa ou comparacao visual entre multiplas telas permanecem manuais, pois o custo de automatizar ainda supera o beneficio nesta fase do projeto.

## Resumo geral da decisao

Automatizados: cenarios de alta repeticao, criterio objetivo de aprovacao e baixa dependencia de percepcao humana.
Manuais: cenarios pontuais, que exigem comparacao visual, analise de contexto ou dependem de fatores externos ao sistema (hardware, dados reais).

Essa divisao busca equilibrar custo de automacao, estabilidade dos cenarios e o objetivo de cada tipo de teste, considerando o time reduzido e o prazo do projeto.
