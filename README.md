# Vesper — releases

Executáveis oficiais do **Vesper para Windows**. Este repositório guarda só as versões publicadas; o código-fonte é privado.

- **Download:** [release mais recente](https://github.com/matheusgsousa/vesper-releases/releases/latest) → `Vesper-windows-x64.exe`
- **Site:** https://vesperbypass.tech/download
- **Integridade:** cada release traz o SHA-256 do executável (`Vesper-windows-x64.exe.sha256` e o digest exibido pelo GitHub). O app só instala atualizações cujo SHA-256 confere.

## Versões

| Data | Versão |
| --- | --- |
| 29/10/2026 | [0.3.2](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.2) |
| 29/10/2026 | [0.3.1](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.1) |
| 29/10/2026 | [0.3.0](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.0) |
| 28/10/2026 | [0.2.3](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.3) |
| 28/10/2026 | [0.2.2](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.2) |
| 28/10/2026 | [0.2.1](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.1) |
| 27/10/2026 | [0.2.0](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.0) |

## Novidades da 0.3.2 — Conexão com outro bypass instalado e Discord reaberto na rota nova

Publicada em 29/10/2026.

**Clicar em Conectar agora funciona mesmo com outro bypass do Discord no computador, e o Discord reabre já pelo túnel.**

### Correções
- **Outro bypass do Discord instalado.** Se o WireSock do computador foi configurado por outro programa para desviar o Discord (como o GoLiveBypass), o Vesper assume o WireSock ao conectar. Um WireSock usado para outra coisa continua intocado.
- **O botão não fica mais mudo.** Na 0.3.1, um erro logo depois da instalação era descartado e nada aparecia na tela. Agora a mensagem aparece.
- **Instalação do WireSock mais segura.** O instalador é baixado para a pasta protegida do Vesper e só roda se tiver a assinatura digital válida do fabricante do WireSock. Antes, o Vesper podia executar um arquivo da pasta temporária do usuário.

### Novidades
- **O Discord reabre sozinho.** Depois de conectar, o Vesper fecha e abre o Discord de novo (ou só abre, se estiver fechado), porque o túnel só vale para conexões novas.
- **Registro no Windows.** Quando substitui o WireSock de outro programa, o Vesper registra isso no Visualizador de Eventos (Aplicativo, origem `VesperVpn`).

### Requisitos
- Windows 10/11 x64 com WebView2.
- Assinatura ativa.

### Limites da prévia
- Há um único servidor real, na Bélgica. As outras regiões são demonstrativas.
- O outro bypass do Discord para de funcionar enquanto o Vesper estiver com o WireSock.

## Requisitos

- Windows 10 22H2 ou Windows 11, 64 bits, com .NET Framework 4.8 e Microsoft Edge WebView2 Runtime (já presentes no Windows atualizado).
- O app roda como usuário comum. Na primeira conexão real, o Windows pede permissão de administrador uma vez, para instalar o componente de rede.

## Prévia

Conta, assinatura (Mercado Pago) e o túnel do Discord para assinantes são reais. Sem assinatura ou no modo demonstração, a conexão é simulada e assim identificada no app. Há um único servidor real, na Bélgica.

O executável ainda não tem assinatura digital: se o SmartScreen aparecer, confira o SHA-256 e clique em "Mais informações" → "Executar assim mesmo".

O Vesper é software proprietário e independente, sem afiliação oficial com o Discord. Avisos de terceiros: `Vesper-NOTICES.txt` em cada release.

<!-- Gerado pelo CI do repositório privado matheusgsousa/vesper. Não edite aqui; veja AGENTS.md. -->
