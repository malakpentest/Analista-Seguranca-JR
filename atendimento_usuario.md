# 🎧 Atendimento ao Usuário: Suporte e Resposta a Incidentes de Segurança

O elo mais importante na segurança da informação é a pessoa que está na ponta operando o sistema. Este documento descreve o fluxo prático de atendimento a usuários que relatam incidentes, suspeitas de ataques ou comportamentos anômalos em seus dispositivos corporativos.

---

## 🎯 Abordagem e Postura do Analista

O atendimento de um Analista de Segurança Júnior deve ser **consultivo, empático e educativo**, nunca punitivo. O objetivo é transformar o usuário em um aliado da segurança (sensor humano), garantindo que ele não tenha medo de reportar erros.

* **Escuta Ativa e Empatia:** O usuário pode estar assustado por ter clicado em um link suspeito. Mantenha a calma e conduza a conversa de forma profissional.
* **Agilidade na Resposta:** Em segurança, minutos contam. Uma contenção rápida evita que um malware se espalhe pela rede ou que credenciais sejam aproveitadas em fraudes.
* **Clareza na Comunicação:** Evite jargões técnicos excessivos ao falar com áreas de negócio; explique o que aconteceu e quais serão os próximos passos de forma simples.

---

## 📋 Passo a Passo do Atendimento (Fluxo de Chamado)

1. **Recepção e Classificação do Chamado:**
   * Identificar o nível de urgência (ex: usuário digitou senha em site falso vs. recebeu um e-mail estranho, mas não interagiu).
2. **Instruções Imediatas de Contenção (Se necessário):**
   * *Caso o usuário tenha executado um arquivo ou colocado credenciais:* Orientar a desconectar a máquina da rede imediatamente (remover cabo de rede / desativar Wi-Fi) e não reiniciar o computador para preservar evidências na memória/logs.
3. **Coleta de Evidências:**
   * Solicitar o encaminhamento do e-mail suspeito como anexo (`.eml`).
   * Anotar o nome do equipamento, usuário, horário exato da ocorrência e ações realizadas pelo colaborador.
4. **Tratativa Técnica (Ações de Resposta):**
   * Revogação imediata de sessões ativas do usuário no diretório centralizado (IAM).
   * Redefinição forçada de senha temporária.
   * Acionamento da equipe de EDR/Antivírus para varredura ou isolamento remoto da estação de trabalho.
5. **Orientação Educativa de Fechamento:**
   * Explicar o que causou o alerta, reforçar a importância de não repetir a ação e agradecer o usuário por ter reportado o caso rapidamente.

---

## 💬 Exemplo Prático de Diálogo / Roteiro de Apoio

* **Usuário:** *"Olá! Acho que cliquei em um link de uma fatura pendente por engano e coloquei minha senha corporativa lá..."*
* **Analista:** *"Olá! Obrigado por avisar imediatamente, você agiu da forma correta e rápida. Para garantirmos a segurança, por favor, mantenha sua máquina conectada ou desconecte da internet se preferir, mas não feche as abas. Vou realizar o bloqueio preventivo da sua conta agora mesmo e redefinir sua senha com segurança. Já estou abrindo a triagem aqui, ok?"*
