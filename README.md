# Nós em Nós · landing pages

Site estático (HTML + CSS + JS, sem build) publicado no GitHub Pages.

| Página | Arquivo | Status |
|---|---|---|
| Página inicial (podcast, quem somos, e-books, contato) | `index.html` | no ar |
| Aula aberta 17/11 (captação de leads) | `aula/index.html` | no ar |
| E-books | `ebooks/index.html` | no ar |

**Página inicial:** o que muda com a fase (faixa do topo, status da temporada, último episódio, quadro da aula) fica no `CONFIG`, no fim do `index.html`. A faixa e o quadro da aula somem sozinhos depois de `aula.ate`.

## Editar sem mexer no código
Tudo que muda com frequência fica em **[`config.js`](config.js)**:

- `planilhaUrl`: para onde vão as inscrições ([como conectar ao Google Planilhas](docs/google-planilhas.md))
- `whatsappGrupoUrl`: grupo para onde a pessoa vai depois de se inscrever
- `instagram`: perfis que aparecem no rodapé

Enquanto `planilhaUrl` estiver vazio, a página funciona em **modo prévia**: o formulário mostra a confirmação, mas **não salva** a inscrição.

## Estrutura
```
index.html              página inicial
aula/index.html         página da aula aberta
ebooks/                 página dos e-books
config.js               links e configurações da aula
assets/inicio           imagens da página inicial
assets/css/style.css    visual (cores da marca em :root)
assets/js/inscricao.js  formulário: validação, envio, redirecionamento
assets/img, assets/fonts
apps-script/Code.gs     script que grava as inscrições na planilha
docs/                   guias
```

## Testar localmente
```bash
python3 -m http.server 8000
```
e abra http://localhost:8000
