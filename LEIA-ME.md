# Site Manuscrito — pacote de hospedagem

Site estático (HTML, CSS e JavaScript simples). Não precisa de servidor, banco de dados nem instalação.

## Estrutura
- `index.html` — página inicial
- `softwares/`, `literario/`, `academico/`, `digital/`, `estudio/`, `diagrama/`, `suite/`, `sobre/`, `contato/`, `privacidade/` — uma página por pasta (endereços como `seusite.com.br/literario/`)
- `404.html` — página de erro
- `assets/img/` — telas dos softwares (WebP) e logo
- `assets/icons/` — os seis ícones em SVG
- `assets/css/style.css` e `assets/js/` — estilo e comportamento
- `assets/js/config.js` — configuração do formulário

## 1. Publicar de graça (escolha uma opção)
Os nomes de menus podem mudar com o tempo; o princípio é o mesmo.

**Opção A — Netlify (a mais simples).** Crie uma conta, abra o recurso "Netlify Drop" (app.netlify.com/drop) e arraste **a pasta inteira** `manuscrito-site`. O site entra no ar em um endereço do tipo `nome.netlify.app`.

**Opção B — Cloudflare Pages.** Crie uma conta, vá em Workers & Pages > Pages e escolha enviar arquivos (upload direto). Envie a pasta.

**Opção C — GitHub Pages.** Crie um repositório, envie os arquivos para a raiz e ative Settings > Pages. O endereço fica `usuario.github.io/repositorio/`. Os links do site são relativos e funcionam nesse formato.

Para atualizar depois, basta enviar a pasta de novo (ou os arquivos alterados, no GitHub).

## 2. Testar antes de divulgar
- Abra o endereço no computador e no celular, nos modos claro e escuro.
- Passe por todas as páginas, abra e feche as telas ampliadas, marque a caixa em Contato e clique no botão do formulário.
- Para testar no seu computador sem publicar: abra um terminal na pasta e rode `python -m http.server`, depois acesse `http://localhost:8000`. (Abrir o `index.html` com duplo clique não funciona bem, porque os links usam pastas.)

## 3. Domínio próprio
1. Registre um `.com.br` no Registro.br (exige CPF ou CNPJ) ou um `.com` em um registrador de sua preferência.
2. Na hospedagem escolhida, use a opção de adicionar domínio personalizado e siga as instruções de DNS que ela mostrar. O certificado HTTPS é emitido automaticamente.
3. Com o domínio no ar: cadastre o site no Google Search Console e peça para me gerar o `sitemap.xml` com o endereço final.

## 4. Formulário: pré-seleção do software
Existe **um único** formulário. Na página de cada software, o botão "Tenho interesse" leva à página de Contato já com o software indicado; para o Google Forms abrir com o campo preenchido:
1. No Google Forms, clique em ⋮ (mais) > **Obter link pré-preenchido**.
2. Escolha qualquer opção em "Software de interesse" e clique em **Obter link**.
3. No link copiado aparece algo como `entry.123456789=...`. Copie só o número.
4. Abra `assets/js/config.js` e preencha `entrySoftware:"123456789"`.

As opções do campo no Forms devem ter exatamente estes nomes: Manuscrito Literário, Manuscrito Acadêmico, Manuscrito Digital, Manuscrito Estúdio, Manuscrito Diagrama, Manuscrito Suite. Se o nome não bater, o campo abre em branco (sem erro). Enquanto `entrySoftware` estiver vazio, o formulário abre normalmente, sem pré-seleção.

## 5. Como alterar o site
- **Textos:** abra o arquivo `index.html` da página desejada em um editor de texto e altere o conteúdo entre as marcas.
- **Telas dos softwares:** substitua os arquivos em `assets/img/` mantendo o mesmo nome (formato WebP, cerca de 1365 px de largura).
- **Política de Privacidade:** `privacidade/index.html`. Revise com um advogado antes de divulgar.

## Pendências conhecidas
- Tela do Literário na aparência **Clara** no editor (hoje o "Claro" mostra a central da obra).
- Telas do Digital nas aparências escura e sépia, sem o livro "Verity" (obra protegida por direitos autorais).
- Telas do Acadêmico com texto de exemplo limpo.
- Requisitos do Windows, versão atual e o que acontece depois do formulário.
- `sitemap.xml` e imagem de compartilhamento (dependem do domínio).
