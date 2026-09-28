# Ajustes manuais no perfil GitHub

O `gh` autenticado nesta máquina não tem escopo `user` para editar bio nem API pública estável para fixar repositórios. Faça uma vez no site:

## Bio e link do site

1. Abra [github.com/settings/profile](https://github.com/settings/profile)
2. **Bio** (sugestão):
   ```
   Extensões Chrome, ferramentas desktop e open source.
   ```
3. **Website**: `https://t1ng4.github.io`

## Fixar 6 repositórios

No seu perfil [github.com/T1NG4](https://github.com/T1NG4), clique em **Customize your pins** e selecione:

1. [ripper-search](https://github.com/T1NG4/ripper-search)
2. [TGS-Zgraphic-Public](https://github.com/T1NG4/TGS-Zgraphic-Public)
3. [TGS-Community](https://github.com/T1NG4/TGS-Community)
4. [C0-4](https://github.com/T1NG4/C0-4)
5. [S01-L1](https://github.com/T1NG4/S01-L1)
6. [T1NG4.github.io](https://github.com/T1NG4/T1NG4.github.io)

## Topics (opcional)

Em cada repositório → **About** → adicione topics, por exemplo:

| Repositório | Topics sugeridos |
|-------------|------------------|
| ripper-search | `chrome-extension`, `typescript` |
| TGS-Zgraphic-Public | `desktop`, `launcher` |
| TGS-Community | `community`, `documentation` |

## Personalizar conteúdo

- E-mail e redes: edite `profile-readme/README.md` (comentário `TODO`) e `t1ng4.github.io/src/components/HomeSections.astro` (`mailto:`).
- Novos projetos: adicione em `t1ng4.github.io/src/data/projects.ts` e uma linha na tabela do README de perfil.

## Escopo `gh` (opcional)

Para atualizar bio via CLI no futuro:

```bash
gh auth refresh -h github.com -s user
gh api user -X PATCH -f bio="..." -f blog="https://t1ng4.github.io"
```
