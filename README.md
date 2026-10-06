# Flow Work

O Flow Work é um projeto de interface para uma plataforma de trabalho. No estado atual, o repositório contém principalmente uma tela de login em português, com tema escuro, detalhes em roxo e campos com ícones. A página de dashboard ainda está em desenvolvimento.

> **Estado do projeto:** protótipo de front-end. Não há autenticação, integração com servidor ou persistência de dados implementadas.

## Tecnologias utilizadas

- **HTML5** — estrutura da página de login e dos seus componentes.
- **CSS3** — layout, cores, tipografia, estados de foco e efeitos visuais.
- **Font Awesome 7.3.1** — ícones de e-mail, cadeado e visibilidade da senha, carregados por CDN.
- **Git** — versionamento do projeto.

Não há framework JavaScript, biblioteca de componentes, ferramenta de build ou dependências de projeto configuradas até o momento.

## Estrutura atual

```text
.
├── README.md
├── login.html
├── dashboard.html
├── style.css
└── assets/
    ├── logo sem fundo.png
    ├── logo flow work.jpeg
    ├── login flow work.jpeg
    └── dashboard flow work.jpeg
```

- `login.html`: marcação da tela de login.
- `style.css`: estilos da tela, incluindo o cartão de login e os campos.
- `dashboard.html`: arquivo reservado para o dashboard; ainda sem conteúdo implementado.
- `assets/`: imagens disponíveis no projeto. A tela atual ainda não usa essas imagens para os botões de login social.

## Como visualizar

Como o projeto não usa processo de build, basta abrir `login.html` em um navegador. Também é possível abrir a pasta no VS Code e usar uma extensão de servidor local, como Live Server.

Os ícones dependem do carregamento da folha de estilos do Font Awesome pela internet. Sem conexão ou acesso ao CDN, eles podem não aparecer.

## Acertos até agora

- A tela tem uma identidade visual consistente, com fundo escuro, transparência, desfoque e destaque roxo.
- O formulário usa tipos de campo adequados (`email` e `password`) e validação nativa básica com `required`.
- Os campos estão organizados em grupos posicionados relativamente, permitindo manter os ícones dentro de cada input e alinhados ao centro vertical.
- O CSS separa a estrutura visual em componentes, como `.login-card`, `.input-group`, `.form-options` e `.social-login`.
- O HTML declara idioma e configuração de viewport para dispositivos móveis.

## Erros e pendências identificados

Estes pontos refletem o conteúdo atual do repositório e são itens de melhoria, não necessariamente falhas de execução:

- **Logos dos provedores:** as imagens dos botões sociais usam `https://wikimedia.org` como endereço de imagem. Esse endereço não aponta para arquivos de logo específicos e os ícones aparecem quebrados. Usar imagens locais de `assets/` ou URLs diretas e confiáveis.
- **Login sem integração:** o formulário não tem `action` nem tratamento JavaScript. O navegador pode fazer o envio padrão, mas não existe autenticação implementada.
- **Ícone de senha sem comportamento:** o ícone de olho está visível, mas ainda não alterna entre mostrar e ocultar a senha.
- **Links provisórios:** “Esqueceu a senha?” e “Criar uma conta” apontam para `#`; “Política de privacidade” não tem um destino definido.
- **Responsividade a validar:** o layout ainda não tem regras específicas para telas menores, e `overflow: hidden` no `body` pode cortar conteúdo em viewports baixos.
- **Tipografia:** `Inter` está declarada no CSS, mas não há importação ou arquivo local da fonte; o navegador pode usar uma fonte substituta.
- **Acessibilidade:** os campos dependem de placeholders em vez de rótulos visíveis ou associados; também convém dar nome acessível aos controles de ícone e conferir contraste e navegação por teclado.
- **Idioma da interface:** o documento está em português, mas o divisor exibe “OR”; pode ser substituído por “OU” para manter a consistência.
- **Dashboard:** `dashboard.html` existe, mas ainda está vazio.

## Dúvidas para as próximas etapas

Antes de conectar funcionalidades, vale decidir:

1. O projeto será apenas um protótipo visual ou terá autenticação real?
2. Qual tecnologia será usada no back-end e onde os dados serão armazenados?
3. O login será feito por e-mail e senha, por provedores sociais ou pelos dois métodos?
4. Quais telas e funções o dashboard deverá incluir?
5. A interface deverá oferecer apenas português ou também outros idiomas?
6. As imagens dos provedores sociais devem vir da pasta `assets/` ou de uma biblioteca/serviço externo?

## Como a IA está ajudando

A IA está sendo usada como apoio ao desenvolvimento, não como substituta da validação do projeto. Neste estágio, ela ajudou a:

- investigar por que os ícones de e-mail e senha não ficavam dentro dos respectivos campos;
- identificar que o posicionamento absoluto precisava usar cada `.input-group` como referência;
- ajustar o alinhamento dos ícones e conferir o resultado no navegador;
- registrar no README as tecnologias, os acertos, as pendências e as decisões que ainda precisam ser tomadas.

Uma boa forma de continuar usando IA é descrever o comportamento esperado, pedir mudanças pequenas e específicas e depois conferir o resultado no navegador, testar a navegação por teclado e revisar o código antes de integrar funcionalidades reais.
