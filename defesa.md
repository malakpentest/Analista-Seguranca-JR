# 🛡️ Diretrizes de Defesa e Boas Práticas Corporativas

A segurança defensiva (Blue Team) exige uma postura proativa para mitigar riscos, reduzir a superfície de ataque e garantir a resiliência dos ativos corporativos. Este documento compila as principais práticas de defesa adotadas por um Analista de Segurança Júnior.

---

## 🧱 Princípios de Defesa em Profundidade (Defense-in-Depth)

Nenhuma camada de segurança é 100% infalível por si só. Por isso, a estratégia defensiva baseia-se em múltiplas barreiras concêntricas:
1. **Perímetro:** Firewalls, Web Application Firewalls (WAF) e filtragem de tráfego de borda.
2. **Rede:** Segmentação de rede, controle de acesso baseado em zonas (VLANs) e monitoramento de tráfego interno.
3. **Endpoints:** Instalação de EDR/XDR, bloqueio de dispositivos USB não autorizados e atualizações rigorosas de patches.
4. **Aplicação & Dados:** Criptografia em trânsito (TLS) e em repouso, políticas de controle de acesso estrito e princípio do menor privilégio.

---

## 🔑 Controles de Acesso e Identidade (IAM)

A identidade tornou-se o novo perímetro de segurança corporativo. Os pilares de defesa incluem:
* **Princípio do Menor Privilégio (PoLP):** Garantir que usuários e sistemas tenham acesso apenas aos recursos estritamente necessários para o desempenho de suas funções.
* **Autenticação Multifator (MFA):** Obrigatoriedade de uso de múltiplos fatores de autenticação para todos os colaboradores, mitigando o risco de comprometimento por credenciais vazadas.
* **Gestão de Ciclo de Vida de Contas:** Desprovisionamento imediato de acessos para colaboradores desligados e revisão periódica de privilégios administrativos.

---

## 📋 Checklist de Hardening e Monitoramento Contínuo

* [ ] **Gestão de Vulnerabilidades:** Realização periódica de escaneamentos para identificar falhas conhecidas em softwares e sistemas operacionais.
* [ ] **Monitoramento de Logs (SIEM):** Centralização e análise contínua de eventos de segurança provenientes de servidores, estações de trabalho e firewalls.
* [ ] **Resposta a Incidentes (IR):** Manutenção de um plano de ação claro para contenção rápida de ameaças e mitigação de danos em caso de intrusão.
* [ ] **Backups Regulares (Regra 3-2-1):** Manter 3 cópias dos dados, em 2 mídias diferentes, sendo 1 cópia off-site (isolada da rede) para proteção contra ransomware.

---

## 🎯 O Papel Proativo do Analista Júnior na Defesa

A defesa não se resume apenas a ferramentas automatizadas; ela depende do fator humano e operacional:
* **Análise de Alertas Diários:** Triagem ágil de falsos positivos versus incidentes reais reportados pelas ferramentas de monitoramento.
* **Orientação de Boas Práticas:** Apoio na conscientização de equipes internas sobre a importância de senhas fortes, cuidado com links e reportes imediatos de anomalias.
* **Documentação de Ameaças:** Atualização constante da base de conhecimento com novos padrões de ataque identificados para antecipar futuras tentativas.
