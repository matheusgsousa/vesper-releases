# AGENTS.md — vesper-releases

Instruções para agentes de IA e pessoas que mexem neste repositório.

## O que é este repositório

- Repositório **público** com os executáveis do Vesper para Windows.
- O código-fonte fica no repositório privado `matheusgsousa/vesper`.
- O app (auto-update) e o site (`/download`) leem `releases/latest` daqui.

## Regra principal: tudo vem do CI do `vesper`

As releases, o `README.md` e este `AGENTS.md` são publicados pelo job `publish` de `.github/workflows/vesper-desktop.yml`, no repositório `vesper`, a cada push na `main`. Não edite nada direto aqui: a próxima sincronização sobrescreve.

| Arquivo aqui | Fonte no `vesper` |
| --- | --- |
| Release `vX.Y.Z` (executável, `.sha256`, `Vesper-NOTICES.txt`) | Build do CI na versão de `desktop/package.json` |
| Notas da release | `docs/releases/X.Y.Z.md`, mais o commit de origem (o app não mostra essa linha) |
| `README.md` | `releases-repo/README.template.md` + `desktop/scripts/releases-readme.mjs` |
| `AGENTS.md` | `releases-repo/AGENTS.md` |

## Regras das releases

1. Cada versão gerada pelo cliente tem exatamente uma release aqui, com a tag `vX.Y.Z`.
2. As releases são normais e `latest`, **nunca** *prerelease*, porque `releases/latest` ignora prereleases.
3. O CI nunca sobrescreve uma tag que já existe. Para lançar, aumente a versão em `desktop/package.json` e crie `docs/releases/X.Y.Z.md` no mesmo PR. Sem esse arquivo, o build falha.
4. Os nomes dos assets são fixos: `Vesper-windows-x64.exe`, `Vesper-windows-x64.exe.sha256` e `Vesper-NOTICES.txt`.

## Regras do README.md

1. **Topo: changelog simples.** Uma tabela só com a data (dd/mm/aaaa, horário de Brasília) e o número da versão, da mais nova para a mais antiga, com link para a release.
2. **Resto: detalhes da versão mais nova.** O que mudou, tirado de `docs/releases/X.Y.Z.md`.
3. Requisitos e avisos ficam no fim, em `releases-repo/README.template.md`.

## Como atualizar o README a cada nova release

1. No `vesper`, aumente a versão em `desktop/package.json` (por exemplo, `0.3.2`).
2. Crie `docs/releases/0.3.2.md`:
   - a primeira linha é o título: `# Vesper 0.3.2 · <resumo>`;
   - o resto descreve o que mudou (Novidades, Correções, Requisitos, Limites).
3. Abra o PR e faça o merge na `main`. O CI então:
   - publica a release `v0.3.2` aqui, com essas notas;
   - acrescenta a linha `| dd/mm/aaaa | 0.3.2 |` no topo da tabela "Versões" do README;
   - troca a seção "Novidades da …" pelos detalhes da 0.3.2.
4. Confira o README daqui depois do pipeline. Se algo estiver errado, corrija a fonte no `vesper` e faça um novo push; não edite aqui.

## Para mudar algo

Abra um PR no `vesper`. Mudou o texto do README? Edite o template. Mudou o formato? Edite `releases-readme.mjs` e o teste dele (`releases-readme.test.mjs`). O merge na `main` sincroniza este repositório.
