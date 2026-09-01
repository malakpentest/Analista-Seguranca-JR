# 🎣 Análise e Resposta a Incidentes de Phishing

Este documento detalha o procedimento prático adotado por um Analista de Segurança Júnior para identificar, analisar e mitigar tentativas de phishing direcionadas ao ambiente corporativo.

---

## 🔍 O Fluxo de Análise

Quando um usuário reporta um e-mail suspeito ou um alerta é disparado pelo sistema de monitoramento, o processo de triagem segue as seguintes etapas:

1. **Triagem Inicial:** Avaliação do contexto (remetente, urgência da mensagem, pedidos de credenciais ou anexos executáveis).
2. **Análise de Cabeçalhos (Email Headers):** Verificação de autenticidade para identificar spoofing.
3. **Inspeção de Links e Domínios:** Descoberta do destino real de URLs encurtadas ou mascaradas.
4. **Análise de Anexos:** Verificação de extensões perigosas (ex: `.iso`, `.exe`, `.scr`, macros maliciosas em documentos `.xlsm` ou `.docx`).
5. **Mitigação e Contenção:** Bloqueio de remetentes, domínios e URLs nos gateways de e-mail e proxy/firewall.

---

## 🛠️ Principais Pontos de Verificação (Checklist Técnico)

### 1. Análise de Cabeçalhos (Email Headers)
O cabeçalho revela o caminho real que o e-mail percorreu. Os principais campos analisados são:
* **`Received:`** Mostra os servidores pelos quais a mensagem passou. A leitura deve ser feita de baixo para cima.
* **`From:` vs `Return-Path:` / `Reply-To:`** Em ataques de *spoofing*, o e-mail exibido no campo "De" pode divergir do endereço real de retorno.
* **Registros de Autenticação:**
  * **SPF (Sender Policy Framework):** Valida se o servidor de envio está autorizado pelo domínio remetente.
  * **DKIM (DomainKeys Identified Mail):** Garante que o e-mail não foi alterado no trajeto através de assinatura criptográfica.
  * **DMARC:** Política que unifica SPF e DKIM para definir o que fazer caso falhem (rejeitar ou colocar em quarentena).

### 2. Inspeção de Links (URLs Maliciosas)
Nunca clique diretamente em um link suspeito. O procedimento seguro envolve:
* **Extração da URL:** Copiar o link sem abrir (passando o mouse por cima ou extraindo via ferramenta de leitura de e-mail).
* **Verificação de Desvio (Redirecionamentos):** Identificar se há uso de serviços de encurtamento legítimos (Bitly, TinyURL) para ocultar o destino final.
* **Consulta de Reputação:** Utilização de ferramentas controladas e sandboxes (como VirusTotal, AbuseIPDB ou análise de strings de domínio).

---

## 📋 Simulação de Caso Prático

* **Cenário:** Um usuário do setor financeiro recebe um e-mail com o assunto *"Urgente: Atualização de Dados Cadastrais e Faturamento"*, contendo um link para um site externo que imita o portal de login corporativo.
* **Ações do Analista Júnior:**
  1. **Isolamento:** Solicitar ao usuário que não insira nenhuma credencial e não interaja mais com a mensagem.
  2. **Coleta:** Extrair o arquivo `.eml` (cabeçalho completo e corpo) para análise isolada.
  3. **Validação:** Identificar que o domínio de destino usava técnicas de *Typosquatting* (ex: alteração sutil de letras para enganar o usuário).
  4. **Ação Corretiva:** 
     * Bloqueio imediato da URL no proxy web.
     * Varredura rápida nos logs de autenticação de IAM para confirmar se o usuário chegou a digitar a senha.
     * Caso positivo: Disparo imediato do protocolo de redefinição de senha forçada e revogação de sessões ativas.

---

## 💡 Indicadores de Comprometimento (IoCs) Comuns em Phishing
* Linguagem altamente alarmista ou de falsa urgência ("Sua conta será suspensa em 24h").
* Erros gramaticais grosseiros em comunicações oficiais de marcas conhecidas.
* Links apontando para TLDs (domínios de topo) incomuns ou IPs diretos.
