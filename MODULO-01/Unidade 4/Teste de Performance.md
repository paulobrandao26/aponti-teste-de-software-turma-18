# Relatório de Teste de Performance (Cenário Fictício)

**Sistema:** Sistema bancário, nova versão com correção no login e ajuste na exibição do saldo na tela inicial
**Ferramenta:** JMeter
**Ambiente:** Homologação
**Usuários virtuais simulados:** 500 (rampa de subida em 5 minutos)
**Duração do teste:** 15 minutos

## Métricas coletadas

| Métrica | `/login` | `/saldo` | Critério de aceite |
|---|---|---|---|
| Tempo médio de resposta | 1.850 ms | 620 ms | ≤ 800 ms |
| Tempo de resposta (p95) | 4.200 ms | 1.100 ms | ≤ 1.500 ms |
| Taxa de erro | 7,3% | 0,2% | ≤ 1% |
| Throughput | 85 req/s | — | ≥ 150 req/s |
| Uso de CPU (servidor) | 96% (pico) | — | ≤ 80% |
| Uso de memória (servidor) | 89% (pico) | — | ≤ 75% |
| Conexões simultâneas no banco | 480/500 (quase esgotado) | — | — |

---

## Respostas

### 1. O sistema pode ser considerado aprovado?
Não. O endpoint `/login` — justamente a área alterada nessa versão, ficou muito acima dos critérios de aceite em tempo de resposta, taxa de erro e throughput.

### 2. Quais métricas indicam problemas de performance?
Tempo de resposta e taxa de erro do `/login`, throughput geral abaixo da meta, uso de CPU/memória do servidor no limite e pool de conexões do banco quase esgotado.

### 3. Quais possíveis gargalos podem existir?
- Correção do login pode ter tornado a validação mais pesada
- Falta de índice na consulta de usuários/sessões
- Pool de conexões com o banco subdimensionado
- Ausência de cache para validações repetitivas
- CPU do servidor de autenticação saturando (subdimensionamento)

### 4. Esse cenário se aproxima mais de Carga, Stress ou Capacidade?
**Carga** — o teste simulou um volume de uso esperado (500 usuários simultâneos, cenário de "dia a dia"), e não um pico extremo intencional (Stress) nem um teste voltado a identificar o limite máximo do sistema (Capacidade).

### 5. O que você recomendaria ao time técnico?
- Investigar e otimizar o endpoint `/login`, com foco na correção recente aplicada
- Revisar índices das tabelas envolvidas na autenticação
- Redimensionar o pool de conexões com o banco de dados
- Avaliar cache para validações de sessão e escalabilidade horizontal do serviço
- Reexecutar o teste após as correções e **não promover a versão para produção** até atingir os critérios de aceite
