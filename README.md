# Vesper — releases

Executáveis oficiais do **Vesper para Windows**. Este repositório guarda só as versões publicadas; o código-fonte é privado.

- **Download:** [release mais recente](https://github.com/matheusgsousa/vesper-releases/releases/latest) → `Vesper-windows-x64.exe`
- **Site:** https://vesperbypass.tech/download
- **Integridade:** cada release traz o SHA-256 do executável (`Vesper-windows-x64.exe.sha256` e o digest exibido pelo GitHub). O app só instala atualizações cujo SHA-256 confere.

## Versões

| Data | Versão |
| --- | --- |
| 29/10/2026 | [0.3.3](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.3) |
| 29/10/2026 | [0.3.2](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.2) |
| 29/10/2026 | [0.3.1](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.1) |
| 29/10/2026 | [0.3.0](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.0) |
| 28/10/2026 | [0.2.3](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.3) |
| 28/10/2026 | [0.2.2](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.2) |
| 28/10/2026 | [0.2.1](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.1) |
| 27/10/2026 | [0.2.0](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.0) |

## Novidades da 0.3.3 — Correção no instalador do WireSock SDK e conexão direta à rota

Publicada em 29/10/2026.

**A instalação automática em segundo plano do WireSock agora baixa o pacote SDK correto com o wiresock-client e flags silenciosas compatíveis.**

### Correções
- **Pacote correto do WireSock.** A rotina de instalação automática do serviço de rede agora baixa o WireSock Secure Connect SDK (`product=wiresock-secure-connect-sdk`), que contém o executável `wiresock-client.exe` em `sdk\wiresock-client.exe`. A versão anterior baixava o instalador padrão sem SDK, que não incluía o `wiresock-client.exe`.
- **Flags silenciosas compatíveis com WiX Burn.** O executável de instalação do WireSock é executado com as opções `/quiet /norestart` próprias de instaladores WiX Burn, em vez de `/S` (parâmetro NSIS que causava falha silenciosa).
- **Atualização do serviço de rede.** A detecção automática de versão do serviço garante que o novo executável do serviço substitua qualquer versão anterior instalada em `Program Files\Vesper\VesperService.exe`.

### Requisitos
- Windows 10/11 x64 com WebView2.
- Assinatura ativa.

### Limites da prévia
- Há um único servidor real, na Bélgica (`74.152.32.90:51820`). As outras regiões são demonstrativas.

## Requisitos

- Windows 10 22H2 ou Windows 11, 64 bits, com .NET Framework 4.8 e Microsoft Edge WebView2 Runtime (já presentes no Windows atualizado).
- O app roda como usuário comum. Na primeira conexão real, o Windows pede permissão de administrador uma vez, para instalar o componente de rede.

## Prévia

Conta, assinatura (Mercado Pago) e o túnel do Discord para assinantes são reais. Sem assinatura ou no modo demonstração, a conexão é simulada e assim identificada no app. Há um único servidor real, na Bélgica.

O executável ainda não tem assinatura digital: se o SmartScreen aparecer, confira o SHA-256 e clique em "Mais informações" → "Executar assim mesmo".

O Vesper é software proprietário e independente, sem afiliação oficial com o Discord. Avisos de terceiros: `Vesper-NOTICES.txt` em cada release.

<!-- Gerado pelo CI do repositório privado matheusgsousa/vesper. Não edite aqui; veja AGENTS.md. -->
