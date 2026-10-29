# Vesper — releases

Executáveis oficiais do **Vesper para Windows**. Este repositório guarda só as versões publicadas; o código-fonte é privado.

- **Download:** [release mais recente](https://github.com/matheusgsousa/vesper-releases/releases/latest) → `Vesper-windows-x64.exe`
- **Site:** https://vesperbypass.tech/download
- **Integridade:** cada release traz o SHA-256 do executável (`Vesper-windows-x64.exe.sha256` e o digest exibido pelo GitHub). O app só instala atualizações cujo SHA-256 confere.

## Versões

| Data | Versão |
| --- | --- |
| 29/10/2026 | [0.3.1](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.1) |
| 29/10/2026 | [0.3.0](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.0) |
| 28/10/2026 | [0.2.3](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.3) |
| 28/10/2026 | [0.2.2](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.2) |
| 28/10/2026 | [0.2.1](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.1) |
| 27/10/2026 | [0.2.0](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.0) |

## Novidades da 0.3.1 — Automação completa do túnel e conexão invisível

Publicada em 29/10/2026.

**Com assinatura ativa, o Discord passa de verdade pelo túnel WireGuard com um único clique. Todo o provisionamento do serviço e do WireSock ocorre de forma transparente em segundo plano.**

### Novidades
- **Conexão simplificada e invisível:**
  - O app configura automaticamente o serviço Windows `VesperVpn` e o WireSock silenciosamente no primeiro clique em "Conectar o Discord".
  - Removidas todas as telas de configuração manual e solicitações de instalação de componentes de rede.
  - Usuários assinantes conectam diretamente ao túnel real sem nenhuma etapa de demonstração ou simulação intermediária.
- **Split tunneling WireGuard:**
  - Tráfego exclusivo para `Discord` e `Update` (`AllowedApps = Discord, Update`).
  - Jogos, streams e navegadores continuam na conexão normal sem penalidade de ping.
- **Proteções do cliente:**
  - Não sobrescreve configurações de WireSock pertencentes a outros softwares (`WIRESOCK_IN_USE`).
  - Desconexão segura e limpeza de túnel ao encerrar sessão ou na expiração da assinatura.

### Requisitos
- Windows 10/11 x64 com WebView2.
- Assinatura ativa.

### Download
- `Vesper-windows-x64.exe`, com SHA-256 nas notas da release e no arquivo `.sha256`.
- `Vesper-NOTICES.txt`.

## Requisitos

- Windows 10 22H2 ou Windows 11, 64 bits, com .NET Framework 4.8 e Microsoft Edge WebView2 Runtime (já presentes no Windows atualizado).
- O app roda como usuário comum. Na primeira conexão real, o Windows pede permissão de administrador uma vez, para instalar o componente de rede.

## Prévia

Conta, assinatura (Mercado Pago) e o túnel do Discord para assinantes são reais. Sem assinatura ou no modo demonstração, a conexão é simulada e assim identificada no app. Há um único servidor real, na Bélgica.

O executável ainda não tem assinatura digital: se o SmartScreen aparecer, confira o SHA-256 e clique em "Mais informações" → "Executar assim mesmo".

O Vesper é software proprietário e independente, sem afiliação oficial com o Discord. Avisos de terceiros: `Vesper-NOTICES.txt` em cada release.

<!-- Gerado pelo CI do repositório privado matheusgsousa/vesper. Não edite aqui; veja AGENTS.md. -->
