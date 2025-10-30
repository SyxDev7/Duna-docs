# Manual do Usuário DunaBot: Guia Completo de Administração

**Bem-vindo(a) ao DunaBot!**

O DunaBot é a ferramenta definitiva para gerenciar e proteger sua comunidade no Telegram. Com uma interface amigável e recursos avançados, você terá controle total sobre seu grupo, automatizando tarefas de moderação e segurança.

---

## 1. O Poder do Sistema de Clones: Sua Própria Instância do Bot

O DunaBot utiliza uma tecnologia **multi-bot** que permite que você tenha sua própria cópia (ou "Clone") do bot.

**Por que usar um Clone?**
*   **Controle Total:** Seu bot, seu token, seu nome. Você tem total autonomia sobre a instância.
*   **Performance Dedicada:** Sua instância não compete por recursos com outros usuários, garantindo agilidade nas respostas.
*   **Configurações Exclusivas:** Todas as configurações e dados são isolados na sua instância.

### 1.1. Como Criar Seu Clone (Via Botão Rápido)

Qualquer usuário pode criar sua própria instância do bot de forma rápida e fácil, sem depender do administrador principal.

1.  **Inicie uma Conversa:** Vá para o chat privado com o bot principal do DunaBot e envie o comando `/start`.
2.  **Clique no Botão:** Na mensagem de boas-vindas, clique no botão **"🤖 Criar um Clone"**.
3.  **Siga as Instruções:** O bot iniciará um processo conversacional, guiando você pelas seguintes etapas:
    *   **Criação no @BotFather:** Você será instruído a ir ao @BotFather, criar seu bot e obter o **TOKEN** de acesso.
    *   **Envio do Token:** Você enviará o token de acesso de volta para o DunaBot.
    *   **Início do Clone:** O DunaBot validará o token, registrará seu novo clone e o colocará online imediatamente.

**Pronto!** Seu bot clone estará online e pronto para ser adicionado aos seus grupos. Você pode configurá-lo com o comando `/settings` no seu grupo.

**Comandos de Gerenciamento de Clones (Apenas para o Owner):**
*   `/clones`: Abre o painel de controle para ver o status (Online/Offline) de todos os seus clones e gerenciá-los (iniciar, parar, remover).
*   `/mybots`: Lista todos os clones registrados no seu sistema.
*   `/delbot <username/id>`: Remove um clone e todos os seus dados do sistema.

---

## 2. Primeiros Passos no Seu Grupo

Para que o DunaBot funcione corretamente, siga estes passos:

1.  **Adicione o Bot:** Convide seu bot clone para o grupo.
2.  **Defina como Administrador:** Promova o bot a administrador do grupo, garantindo as seguintes permissões mínimas:
    *   **Excluir Mensagens** (essencial para Anti-Spam e Blacklist)
    *   **Banir Usuários** (essencial para Mute, Kick, Warns e Captcha)
    *   **Fixar Mensagens** (para o módulo de Pins)
    *   **Adicionar Novos Administradores** (não é obrigatório, mas recomendado para o funcionamento completo).

---

## 3. O Painel de Configurações (`/settings`)

A maneira mais fácil e completa de configurar o DunaBot é através do painel *inline*.

**Como Acessar:**
1.  No seu grupo, digite o comando `/settings`.
2.  O bot enviará uma mensagem no grupo com um botão **"⚜️ Abrir Configurações ⚜️"**.
3.  Clique no botão. O painel será aberto no seu chat privado com o bot.

O painel é dividido em módulos:

### 3.1. Módulo de Boas-Vindas (👋)

Gerencie a mensagem que novos membros recebem.

| Configuração | Descrição |
| :--- | :--- |
| **Status da Mensagem** | Ativa ou desativa a mensagem de boas-vindas. |
| **Status do Captcha** | Ativa ou desativa o sistema Anti-bot (Captcha) para novos membros. |
| **Construtor de Boas-Vindas** | Permite definir: **Texto** (com variáveis como `{user_mention}`), **Mídia** (Foto/GIF) e **Botões *Inline***. |
| **Apagar Anterior** | Define se a última mensagem de boas-vindas deve ser apagada ao entrar um novo membro. |
| **Apagar Após...** | Configura um tempo (em minutos) para que a mensagem de boas-vindas seja auto-destruída. |

### 3.2. Módulo de Advertências (🛡️)

Configure o sistema de *Warns* (Advertências).

| Configuração | Descrição |
| :--- | :--- |
| **Limite Atual** | Define o número de advertências que um usuário pode receber antes de ser **automaticamente banido** do grupo (padrão é 3). |
| **Definir Limite** | Permite ajustar o limite de advertências (entre 2 e 10). |

### 3.3. Módulo Anti-Spam (🛡️)

Proteja seu grupo contra links e spam.

| Configuração | Descrição |
| :--- | :--- |
| **Status Atual** | Ativa ou desativa o Anti-Spam (apaga links de não-admins). |
| **Gerenciar Whitelist** | Adicione domínios ou padrões de link que **não** devem ser apagados pelo bot (ex: `youtube.com`, `t.me/seu_canal`). |

### 3.4. Módulo Anti-Flood (🛡️)

Previna que usuários enviem mensagens em sequência muito rapidamente.

| Configuração | Descrição |
| :--- | :--- |
| **Status Atual** | Ativa ou desativa o Anti-Flood. |
| **Ajustar Sensibilidade** | Define o limite de mensagens e o tempo (ex: 5 mensagens em 3 segundos). |
| **Definir Punição** | Escolha a ação do bot ao detectar um flood: **Advertir**, **Silenciar** (Mute) ou **Remover** (Kick). |

### 3.5. Módulo de Filtros (🚦)

Bloqueie o envio de mídias específicas por membros comuns.

| Filtro | Descrição |
| :--- | :--- |
| **Stickers / GIFs** | Bloqueia o envio de figurinhas e GIFs animados. |
| **Mensagens de Voz** | Bloqueia o envio de áudios. |
| **Encaminhamentos** | Bloqueia o encaminhamento de mensagens de outros chats. |
| **Enquetes / Arquivos** | Bloqueia o envio de enquetes e arquivos em geral. |

### 3.6. Módulo de Logs (📣 e 📝)

Configure canais privados para rastrear a atividade do grupo.

| Módulo | Descrição |
| :--- | :--- |
| **Reports (📣)** | Defina um canal para onde o bot enviará as denúncias feitas por membros com o comando `/report`. O bot adiciona botões de ação rápida (Banir, Advertir, etc.) no log. |
| **Logs de Auditoria (📝)** | Defina um canal para registrar todas as ações administrativas (mudanças de configuração, moderação, etc.), mantendo um histórico completo. |

### 3.7. Módulo de Limpeza (🧹)

Gerencie a remoção de contas excluídas e o Modo Noite.

| Configuração | Descrição |
| :--- | :--- |
| **Limpeza Automática** | Ativa a remoção diária automática de "Contas Excluídas" do grupo. |
| **Modo Noite (🌙)** | Ativa o fechamento (`/lock`) e a reabertura (`/unlock`) automáticos do grupo em horários definidos por você (ex: 22:00-07:00). |

### 3.8. Módulo de Respostas (💬)

Crie respostas automáticas (Notas ou Comandos Customizados) para palavras-chave ou comandos.

*   **Criar Novo Filtro:** Defina um nome, os gatilhos (palavras-chave) e a mensagem de resposta (que pode incluir mídia e botões).
*   **Apagar um Filtro:** Remova uma resposta automática existente.

---

## 4. Guia de Comandos Rápidos

O DunaBot também pode ser controlado diretamente no grupo via comandos.

### 4.1. Comandos de Moderação (Apenas Admins)

| Comando | Uso | Descrição |
| :--- | :--- | :--- |
| `/ban` | Responda à mensagem ou `/ban @usuario [motivo]` | Bane o usuário permanentemente do grupo. |
| `/kick` | Responda à mensagem ou `/kick @usuario [motivo]` | Remove o usuário do grupo (ele pode retornar com um novo link). |
| `/mute` | Responda à mensagem ou `/mute @usuario [tempo]` | Silencia o usuário pelo tempo especificado (Ex: `10m`, `2h`, `1d`). |
| `/unban`, `/unmute` | `/unban @usuario` ou `/unmute @usuario` | Remove o banimento ou o silenciamento. |
| `/warn` | Responda à mensagem ou `/warn @usuario [motivo]` | Adverte o usuário. Ao atingir o limite, ele é banido. |
| `/warnings` | Responda à mensagem ou `/warnings @usuario` | Vê o histórico de advertências de um usuário. |
| `/rmwarn` | Responda à mensagem do usuário | Remove a advertência mais recente do usuário. |
| `/lock` | `/lock` | Fecha o grupo (Modo Lockdown), permitindo apenas mensagens de administradores. |
| `/unlock` | `/unlock` | Abre o grupo, permitindo que todos os membros enviem mensagens. |
| `/pin` | Responda à mensagem | Fixa a mensagem no topo do grupo. |
| `/unpin` | Responda à mensagem | Desfixa a mensagem. |
| `/unpinall` | `/unpinall` | Desfixa todas as mensagens do grupo. |
| `/deleta` | Responda à primeira mensagem da faixa | Inicia a deleção em massa de mensagens a partir daquela que foi respondida. |
| `/limpar` | `/limpar` | Inicia o processo de remoção de Contas Excluídas. |

### 4.2. Comandos de Configuração Rápida (Apenas Admins)

| Comando | Uso | Descrição |
| :--- | :--- | :--- |
| `/addbl` | `/addbl [palavra ou frase]` | Adiciona uma palavra à Blacklist. |
| `/rmbl` | `/rmbl [palavra ou frase]` | Remove uma palavra da Blacklist. |
| `/addfilter` | `/addfilter <gatilho> <resposta>` | Cria um filtro de resposta automática simples. |
| `/delfilter` | `/delfilter <gatilho>` | Apaga um filtro de resposta. |
| `/backup` | `/backup` | Gera um arquivo de backup das configurações do grupo. |
| `/restore` | Responda ao arquivo de backup com `/restore` | Restaura as configurações do grupo. |
| `/send` | `/send [texto com Markdown]` ou responda a uma mensagem | Envia uma nova mensagem com formatação avançada ou reenvia uma mensagem. |
| `/reload` | `/reload` | Atualiza o cache de administradores do bot. |

### 4.3. Comandos de Membros (Todos)

| Comando | Uso | Descrição |
| :--- | :--- | :--- |
| `/start` | `/start` | Mensagem de boas-vindas do bot. |
| `/help` | `/help` | Exibe o menu de ajuda com a lista de comandos. |
| `/regras` | `/regras` | Exibe a mensagem de regras configurada pelos administradores. |
| `/staff` | `/staff` | Lista todos os administradores do grupo. |
| `/info` | Responda à mensagem ou `/info @usuario` | Vê informações detalhadas sobre um usuário. |
| `/id` | `/id @usuario` ou `/id @canal` | Busca o ID de um usuário, grupo ou canal. |
| `/report` | Responda à mensagem | Envia uma denúncia sobre a mensagem para os administradores. |
| `/filters` | `/filters` | Lista todos os filtros de resposta (comandos customizados) ativos no grupo. |

---
*Este manual foi elaborado para garantir que você e sua equipe possam utilizar todos os recursos do DunaBot com máxima eficiência.*
