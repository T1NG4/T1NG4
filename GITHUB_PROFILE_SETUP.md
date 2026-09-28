# Ajustes manuais no perfil GitHub

O `gh` autenticado nesta máquina não tem escopo `user` para editar bio nem API pública estável para fixar repositórios. Faça uma vez no site:

## Bio e link do site

1. Abra [github.com/settings/profile](https://github.com/settings/profile)
2. **Bio** (sugestão):
   ```
   Apps Windows, extensões Chrome e ferramentas para comunidades.
   ```
3. **Website**: `https://t1ng4.github.io`

## Fixar 6 repositórios

No seu perfil [github.com/T1NG4](https://github.com/T1NG4), clique em **Customize your pins** e selecione, nesta ordem:

1. [TGS-Community](https://github.com/T1NG4/TGS-Community) — ecossistema principal (site: [tgs.gamer.gd](https://tgs.gamer.gd/))
2. [TGS-Site](https://github.com/T1NG4/TGS-Site) — código do site oficial
3. [ripper-search](https://github.com/T1NG4/ripper-search) — extensão na Chrome Web Store
4. [TGS-Zgraphic-releases](https://github.com/T1NG4/TGS-Zgraphic-releases) — Zgraphic Launcher
5. [TGS-SPRAY-interception-releases](https://github.com/T1NG4/TGS-SPRAY-interception-releases) — treino de recoil
6. [T1NG4.github.io](https://github.com/T1NG4/T1NG4.github.io) — portfólio

Os repos `S01-L1`, `C0-4` e `TGS-Zgraphic-Public` saíram dos pins: os dois primeiros são acadêmicos e o último está vazio (o conteúdo real está em `TGS-Zgraphic-releases`).

## Descrições faltando

Estes repos públicos aparecem sem descrição no GitHub. Vale preencher o campo **About**:

| Repositório | Sugestão |
|-------------|----------|
| TGS-Zgraphic-Public | Arquivar ou apontar para `TGS-Zgraphic-releases` |
| C0-4 | Dicionário de língua fictícia em C++ com grafo e coordenadas 3D |
| TGS-Site | Landing page e catálogo da TGS Store em HTML/CSS/JS |
| TGS-Community | Monorepo do ecossistema TGS para FiveM |

## Personalizar conteúdo

- Contato: `t1ng4.github.io/src/components/HomeSections.astro` (GitHub e Discord já configurados)
- Novos projetos: adicione em `t1ng4.github.io/src/data/projects.ts` — a home, o grid e a página de detalhe em ambos os idiomas são geradas a partir desse arquivo
- Para destacar um projeto na home, marque `featured: true`

## Escopo `gh` (opcional)

Para atualizar bio via CLI no futuro:

```bash
gh auth refresh -h github.com -s user
gh api user -X PATCH -f bio="..." -f blog="https://t1ng4.github.io"
```
