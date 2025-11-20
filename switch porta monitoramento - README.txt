# Monitoramento de Portas + Alertas Telegram

Este script em PowerShell captura logs de switches via syslog UDP (porta 514) e envia alertas de mudanças de estado de portas para o Telegram.

---

## Passo a passo para usar este script no GitHub

### 1. Salvar o arquivo
- Abra o Bloco de Notas ou VSCode.
- Copie o conteúdo do script fornecido.
- Salve como `MonitorSwitchPorts.ps1`.

### 2. Editar configurações
- Substitua `<SEU_BOT_TOKEN_AQUI>` pelo token do seu bot Telegram.
- Substitua `<SEU_CHAT_ID_AQUI>` pelo seu Chat ID.
- Se desejar, ajuste os caminhos `$StatusDir` e `$LogFile`.

### 3. Configurar switches
- Troque os IPs, nomes e portas do array `$switches` para refletirem seu ambiente real.

Exemplo:
"192.168.1.10|CORE|Fa0/1:servidor,Fa0/2:firewall"

### 4. Executar o script
- Abra o PowerShell como Administrador.
- Execute os comandos:

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser  
.\MonitorSwitchPorts.ps1

---

> ⚠️ Atenção: Este é apenas um exemplo. Em um ambiente real, altere as configurações para os IPs, portas e nomes corretos do seu ambiente.
