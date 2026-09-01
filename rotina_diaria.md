# 📅 Rotina Diária de um Analista de Segurança Júnior (SOC/Operações)

Este documento descreve as atividades recorrentes, o fluxo de priorização e a rotina operacional de um Analista de Segurança da Informação Júnior, unindo monitoramento técnico, suporte ao usuário e melhoria contínua de processos.

---

## 🌅 Período da Manhã: Triagem, Monitoramento e Alertas

O início do turno é dedicado à verificação da saúde do ambiente e à análise de incidentes pendentes ou ocorridos fora do horário comercial.

* **Revisão de Fechamento de Turno (Handover):** Leitura de logs e chamados em aberto deixados pelo turno anterior ou acumulados durante a noite.
* **Monitoramento de Alertas Prioritários:** 
  * Verificação do painel do SIEM/EDR para identificar anomalias em endpoints ou servidores.
  * Checagem de picos de alertas de autenticação suspeita (ex: tentativas de força bruta ou logins de localizações incomuns).
* **Triagem de E-mails Reportados:** Análise dos chamados abertos por colaboradores relatando possíveis e-mails de *phishing* ou anexos suspeitos.
* **Stand-up Operacional:** Alinhamento rápido com a equipe de segurança e infraestrutura sobre incidentes críticos em andamento.

---

## ☀️ Período da Tarde: Resposta, Suporte e Documentação

O segundo período do dia foca na resolução ativa de incidentes, atendimento consultivo a usuários e manutenção preventiva.

* **Tratativa e Contenção de Incidentes:** 
  * Isolamento de máquinas comprometidas na rede (via EDR).
  * Redefinição forçada de credenciais e revogação de sessões para usuários afetados por engenharia social ou phishing.
* **Atendimento Consultivo a Usuários:** Suporte a colaboradores com dúvidas sobre procedimentos de segurança, liberação controlada de acessos ou verificação de links.
* **Análise de Falsos Positivos (Tuning):** Ajuste de regras de alerta no sistema para reduzir o ruído operacional e otimizar a detecção de ameaças reais.
* **Documentação e Atualização de Chamados:** Registro detalhado de cada incidente no sistema de tickets, garantindo o histórico para auditorias e métricas de SLA.

---

## 🌆 Encerramento do Turno: Fechamento e Passagem de Bastão

Antes de finalizar o dia de trabalho, o analista garante que o ambiente esteja documentado e seguro para o próximo período.

* **Revisão de Tickets Pendentes:** Certificar-se de que nenhum chamado crítico ficou sem um status atualizado ou direcionamento.
* **Handover / Relatório Diário:** Registro das ocorrências relevantes do dia em um relatório interno ou passagem de bastão para o próximo turno.
* **Organização de Indicadores:** Consolidação rápida de métricas diárias (número de phishings bloqueados, incidentes triados e chamados atendidos).

---

## 🎯 Pilares do Sucesso na Rotina Diária

1. **Gestão de Prioridades:** Saber diferenciar um alarme crítico real de um falso positivo inofensivo.
2. **Comunicação Assertiva:** Explicar termos técnicos de segurança de forma clara e simples para usuários de outras áreas.
3. **Documentação Rigorosa:** Registrar cada passo da investigação, garantindo conformidade e rastreabilidade.
