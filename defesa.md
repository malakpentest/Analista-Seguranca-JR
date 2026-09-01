# 🛡️ Diretrizes de Defesa e Monitoramento de Alertas

A segurança defensiva (Blue Team) exige uma postura proativa para mitigar riscos, reduzir a superfície de ataque e garantir a resiliência dos ativos corporativos. Este documento compila as principais práticas de defesa e o fluxo de monitoramento de alertas adotados por um Analista de Segurança Júnior.

---

## 🧱 Princípios de Defesa em Profundidade (Defense-in-Depth)

Nenhuma camada de segurança é 100% infalível por si só. Por isso, a estratégia defensiva baseia-se em múltiplas barreiras concêntricas:
1. **Perímetro:** Firewalls, Web Application Firewalls (WAF) e filtragem de tráfego de borda.
2. **Rede:** Segmentação de rede, controle de acesso baseado em zonas (VLANs) e monitoramento de tráfego interno.
3. **Endpoints:** Instalação de EDR/XDR, bloqueio de dispositivos USB não autorizados e atualizações rigorosas de patches.
4. **Aplicação & Dados:** Criptografia em trânsito (TLS) e em repouso, políticas de controle de acesso estrito e princípio do menor privilégio.

---

## 🚨 Monitoramento de Alertas e Triagem (SOC N1)

O monitoramento contínuo é a linha de frente da defesa cibernética. De nada adianta ter barreiras se não houver visibilidade sobre o que acontece no ambiente.

### Principais Fontes de Alertas Monitoradas:
* **EDR (Endpoint Detection and Response):** Detecção de processos suspeitos, scripts maliciosos em PowerShell e conexões de rede atípicas.
* **SIEM / Logs de Autenticação:** Identificação de picos de falhas de login, tentativas de força bruta ou acessos de localizações geográficas anômalas.
* **Gateway de E-mail / Proxy:** Alertas de tráfego direcionado a domínios maliciosos ou tentativas de exfiltração.

### Fluxo Prático de Triagem de Alertas:
1. **Validação:** O alerta é uma ameaça real ou um **falso positivo** (ex: um administrador executando um script legítimo)?
2. **Enriquecimento:** Consulta de reputação de IPs e hashes em bases de inteligência de ameaças.
3. **Classificação e Priorização:** Definição da severidade (Baixa, Média, Alta, Crítica) com base no impacto ao negócio.
4. **Contenção Inicial:** Aplicação de playbooks de resposta (como isolar um host via EDR ou bloquear um IP no firewall).

---

## 🔑 Controles de Acesso e Identidade (IAM)

A identidade tornou-se o novo perímetro de segurança corporativo. Os pilares de defesa incluem:
* **Princípio do Menor Privilégio (PoLP):** Garantir que usuários e sistemas tenham acesso apenas aos recursos estritamente necessários.
* **Autenticação Multifator (MFA):** Obrigatoriedade de uso de múltiplos fatores de autenticação para mitigar comprometimento por credenciais vazadas.
* **Gestão de Ciclo de Vida:** Desprovisionamento imediato de acessos para colaboradores desligados.

---

## 📋 Checklist de Hardening e Monitoramento Contínuo

* [ ] **Gestão de Vulnerabilidades:** Varreduras periódicas para identificar falhas em softwares e sistemas.
* [ ] **Análise de Logs em Tempo Real:** Centralização e acompanhamento de eventos de segurança no SIEM.
* [ ] **Resposta a Incidentes (IR):** Execução de playbooks estruturados para contenção rápida de ameaças.
* [ ] **Backups Regulares (Regra 3-2-1):** 3 cópias de dados, 2 mídias diferentes e 1 cópia off-site isolada contra ransomware.