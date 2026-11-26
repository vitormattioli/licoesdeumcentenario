# licoesdeumcentenario: como publicar

## 1. Coloque seu e-mail na lista de espera
Já configurado para `vitor.fabricadevendas@gmail.com` (variável `EMAIL_DESTINO`, perto do fim do `index.html`).

O formulário usa o FormSubmit (gratuito, sem cadastro). Na **primeira** inscrição feita
no site já publicado, ele manda um e-mail de ativação para esse endereço. Clique no link
de ativação. A partir daí, cada nova inscrição chega na sua caixa de entrada com nome e e-mail.
Faça você mesmo a primeira inscrição de teste.

## 2. Suba no GitHub Pages
1. Crie um repositório no GitHub (ex.: `licoesdeumcentenario`).
2. Envie todo o conteúdo desta pasta para a raiz do repositório
   (`index.html`, `CNAME`, `.nojekyll`, pastas `img/` e `fonts/`).
3. No repositório: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   branch `main`, pasta `/ (root)`. Salve.
4. Em **Custom domain** deve aparecer `licoesdeumcentenario.com.br` (vem do arquivo `CNAME`).
   Se o seu domínio for outro, edite o arquivo `CNAME`.

## 3. Aponte o domínio no Registro.br
No painel do Registro.br, em **DNS → Editar zona**, crie:

| Tipo  | Nome | Valor |
|-------|------|-------|
| A     | (vazio) | 185.199.108.153 |
| A     | (vazio) | 185.199.109.153 |
| A     | (vazio) | 185.199.110.153 |
| A     | (vazio) | 185.199.111.153 |
| CNAME | www  | SEU-USUARIO.github.io |

A propagação pode levar algumas horas. Depois, volte em **Settings → Pages** e marque
**Enforce HTTPS**.

## O que tem aqui
- `index.html`: a página inteira (HTML, CSS e o script do formulário).
- `img/`: fotos do livro, já recortadas e comprimidas.
- `fonts/`: Archivo e Source Serif 4 (licença OFL), hospedadas no próprio site.
