# Vesper — releases

Executáveis oficiais do **Vesper para Windows**. Este repositório guarda só as versões publicadas; o código-fonte é privado.

- **Download:** [release mais recente](https://github.com/matheusgsousa/vesper-releases/releases/latest) → `Vesper-windows-x64.exe`
- **Site:** https://vesperbypass.tech/download
- **Integridade:** cada release traz o SHA-256 do executável (`Vesper-windows-x64.exe.sha256` e o digest exibido pelo GitHub). O app só instala atualizações cujo SHA-256 confere.

## Versões

| Data | Versão |
| --- | --- |
| 29/10/2026 | [0.3.4](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.4) |
| 29/10/2026 | [0.3.3](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.3) |
| 29/10/2026 | [0.3.2](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.2) |
| 29/10/2026 | [0.3.1](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.1) |
| 29/10/2026 | [0.3.0](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.3.0) |
| 28/10/2026 | [0.2.3](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.3) |
| 28/10/2026 | [0.2.2](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.2) |
| 28/10/2026 | [0.2.1](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.1) |
| 27/10/2026 | [0.2.0](https://github.com/matheusgsousa/vesper-releases/releases/tag/v0.2.0) |

## Novidades da 0.3.4 — Região real na tela e novidades formatadas

Publicada em 29/10/2026.

**Com assinatura, a tela mostra o servidor que o túnel usa de verdade: Bruxelas, na Bélgica.**

### Correções
- **Região exibida.** Assinantes viam uma região de demonstração (por exemplo, "Miami · 118 ms") enquanto o tráfego saía pela Bélgica. Agora a saída mostra **Bruxelas · Bélgica · servidor real**.
- **Página de regiões.** Para assinantes, ela mostra o servidor em uso e as outras cidades como *em breve*, sem latência nem ocupação de exemplo. A escolha de região chega numa próxima versão.

### Novidades
- **Novidades da versão formatadas.** O aviso de atualização e a tela Configurações mostram títulos, **negrito**, listas e `código`.
- **Texto inteiro.** As novidades não são mais cortadas: a área rola quando o texto é longo, e o aviso inteiro rola em janelas baixas.

### Limites da prévia
- Há um único servidor real, na Bélgica.
- No modo demonstração, as regiões, latências e ocupações continuam sendo exemplos, identificados na tela.

## Requisitos

- Windows 10 22H2 ou Windows 11, 64 bits, com .NET Framework 4.8 e Microsoft Edge WebView2 Runtime (já presentes no Windows atualizado).
- O app roda como usuário comum. Na primeira conexão real, o Windows pede permissão de administrador uma vez, para instalar o componente de rede.

## Prévia

Conta, assinatura (Mercado Pago) e o túnel do Discord para assinantes são reais. Sem assinatura ou no modo demonstração, a conexão é simulada e assim identificada no app. Há um único servidor real, na Bélgica.

O executável ainda não tem assinatura digital: se o SmartScreen aparecer, confira o SHA-256 e clique em "Mais informações" → "Executar assim mesmo".

O Vesper é software proprietário e independente, sem afiliação oficial com o Discord. Avisos de terceiros: `Vesper-NOTICES.txt` em cada release.

<!-- Gerado pelo CI do repositório privado matheusgsousa/vesper. Não edite aqui; veja AGENTS.md. -->
