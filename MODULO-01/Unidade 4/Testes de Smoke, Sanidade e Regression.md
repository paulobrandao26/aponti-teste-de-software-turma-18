## &#x20;                              **Testes de Smoke**



**Objetivo:** verificar rapidamente se a versão é estável o suficiente pra seguir testando, funcionalidades críticas e básicas, sem profundidade.



\#	Cenário

1	Login com usuário e senha válidos é aceito e redireciona pra tela inicial

2	Tela inicial carrega sem erros/crash após o login

3	Saldo é exibido na tela inicial (mesmo que o valor não seja validado em detalhe)

4	Aplicativo/sistema abre normalmente (sem tela branca, erro 500, etc.)

5	Botão de logout funciona e retorna à tela de login



**Justificativa:** como o smoke test é o primeiro filtro depois de um deploy, os cenários escolhidos cobrem o fluxo mínimo de vida do sistema (entrar → ver a tela principal → sair), tocando exatamente as duas áreas que mudaram (login e saldo), sem entrar em casos alternativos. Se qualquer um desses falhar, não faz sentido investir tempo em testes mais profundos, a build é rejeitada e devolvida pro time de dev.





================================================================================================



## &#x20;                            **teste de sanidade**





**Objetivo:** validar, com mais profundidade, se a funcionalidade especificamente alterada está se comportando corretamente, mais focado que o smoke, porém ainda não tão abrangente quanto a regressão.



\#	Cenário

1	Login com senha incorreta exibe mensagem de erro apropriada (valida a correção feita no login)

2	Login com usuário bloqueado/inexistente é tratado corretamente

3	Saldo exibido na tela inicial corresponde ao valor real da conta (comparado com extrato/banco de dados)

4	Saldo é atualizado corretamente após uma transação simples (ex: PIX recebido) refletindo na tela inicial

5	Formatação do saldo está correta (casas decimais, símbolo de moeda, valores negativos se aplicável)



**Justificativa:** esses cenários miram diretamente nas duas mudanças da versão (login e exibição de saldo), indo além do "funciona ou não" do smoke test pra verificar se a correção realmente resolveu o problema esperado e não introduziu comportamento incorreto nessas áreas específicas — que é exatamente o propósito do sanity test: validar pontualmente o que mudou.





=====================================================================================================





## &#x20;                            **teste de regressao**





**Objetivo:** garantir que as mudanças feitas não quebraram funcionalidades que já funcionavam antes, cobertura ampla, incluindo áreas relacionadas mas não diretamente alteradas.



\#	Cenário

1	Transferências (PIX, TED) continuam funcionando normalmente após o ajuste no saldo da tela inicial

2	Extrato detalhado da conta continua exibindo o histórico de transações corretamente

3	Recuperação de senha ("esqueci minha senha") continua funcionando após a correção no login

4	Login via biometria/token (se existir) continua funcionando, não só login por senha

5	Outras telas que também exibem saldo (ex: tela de transferência, tela de extrato) continuam consistentes com o novo valor exibido na tela inicial



**Justificativa:** como a correção mexeu em login e em exibição de saldo, duas áreas centrais do sistema, usadas como base por várias outras funcionalidades — a regressão precisa confirmar que funcionalidades adjacentes e dependentes (transferências, extrato, outras telas com saldo) não foram afetadas colateralmente. É comum um ajuste "pequeno" numa área central gerar efeito cascata em partes do sistema que dependem dela.

