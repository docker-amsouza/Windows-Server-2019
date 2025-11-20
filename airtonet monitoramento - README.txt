# AIRONET - Monitoramento via Syslog + Alertas Telegram

Este script em PowerShell captura logs de dispositivos conectados a Access Points via syslog UDP (porta 5514) e envia alertas para o Telegram quando dispositivos se conectam, desconectam ou recebem DHCP.

Passo a passo para usar este script no GitHub

1. Salvar o arquivo
- Abra o Bloco de Notas ou Notepad++.
- Copie o conteúdo do script fornecido.
- Salve como AironetMonitoramento.ps1.

2. Editar configurações
- Substitua <SEU_BOT_TOKEN_AQUI> pelo token do seu bot Telegram.
- Substitua <SEU_CHAT_ID_AQUI> pelo seu Chat ID.
- Se desejar, ajuste os caminhos $LOG_PATH e $LOG_FILE.

3. Configurar dispositivos
- Troque os MACs e nomes no array $Hosts para refletirem seu ambiente real.

Exemplo:
"AA:AA:AA:AA:AA:AA" = "tomada-ventilador"
"BB:BB:BB:BB:BB:BB" = "tv-sala"
"CC:CC:CC:CC:CC:CC" = "camera-quarto"

- Configure os APs no array $APs para corresponder aos IPs reais.

Exemplo:
"10.0.0.101" = "AP Sala"
"10.0.0.102" = "AP Quarto"

4. Executar o script
- Abra o PowerShell como Administrador.
- Execute os comandos:

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
.\AironetMonitoramento.ps1

O script ficará em loop monitorando a porta UDP 5514 e enviando alertas ao Telegram.

⚠️ Atenção: Este é apenas um exemplo. Em um ambiente real, altere as configurações para os MACs, IPs, nomes de dispositivos e tokens corretos do seu ambiente.
