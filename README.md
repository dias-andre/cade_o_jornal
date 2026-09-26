# Cadê o Jornal?

O **Cadê o Jornal?** é um jornal digital feito como projeto durante um curso técnico na escola. O site reúne notícias, matérias e informações da Etec de Taboão da Serra, além de páginas sobre eventos, grêmio, monitorias, vestibulares, cultura e tirinhas.

O projeto foi construído com HTML, CSS e JavaScript no navegador. As páginas e os textos são arquivos HTML escritos manualmente: não há servidor, banco de dados, sistema de publicação ou geração dinâmica das páginas. Alguns scripts cuidam de interações da interface e consultam serviços externos para mostrar clima e cotação do dólar.

## Um recado sobre o projeto

Este trabalho foi desenvolvido enquanto eu estudava no curso técnico. **Já me formei e, por isso, não fiz grandes mudanças neste repositório depois de concluir essa etapa.** O conteúdo representa o projeto como ele ficou naquele período; alguns recursos ou informações podem estar desatualizados.

## Como abrir

Não é necessário instalar dependências nem usar um gerenciador de pacotes. Para visualizar o site, abra o arquivo `index.html` em um navegador. Para uma experiência mais consistente, você também pode servir a pasta do projeto com qualquer servidor HTTP local.

O clima e a cotação dependem de acesso à internet e da disponibilidade das APIs usadas pelo JavaScript. Sem conexão, as páginas continuam acessíveis, mas esses dados podem não aparecer.

## Organização dos arquivos

```text
.
├── index.html          # Página inicial, com destaques e lista de notícias
├── pages/              # Páginas temáticas e de serviços da escola
├── noticias/           # Matérias completas e um modelo de matéria
├── assets/             # Logos, ícones e imagens usados na interface
├── images/             # Imagens de capa e conteúdo das matérias
├── css/                # Estilos gerais e estilos específicos das páginas
└── js/                 # Interações da página inicial, eventos e grêmio
```

### Páginas

- `index.html` é a entrada do jornal: apresenta notícias em destaque, cartões de matérias, filtros e o botão para mostrar mais notícias.
- `pages/` contém as páginas de `eventos`, `grêmio`, `monitorias`, `vestibulares`, `cultura` e `tirinhas`.
- `noticias/` contém as matérias completas. O arquivo `template.html` serve como referência para criar novas matérias; os trechos entre chaves, como `{title}` e `{paragraph}`, são marcadores para substituir manualmente no HTML.

### Estilos e imagens

Os arquivos em `css/` definem o visual. `style.css` reúne estilos da página inicial e partes compartilhadas; outros arquivos, como `eventos.css`, `gremio.css` e `noticia1.css`, atendem páginas ou grupos de páginas específicos. `media.css` contém ajustes para telas menores.

As imagens estão divididas entre `assets/`, com logos e ícones reutilizados, e `images/`, com capas e imagens das notícias e eventos. Os caminhos relativos até essas pastas variam conforme a página: ao adicionar uma imagem, confira o caminho a partir do arquivo HTML que vai usá-la.

### JavaScript

- `js/script.js` controla filtros e expansão da lista de notícias, consulta clima e câmbio e implementa ações de curtir, salvar e compartilhar presentes na página inicial.
- `js/eventos.js` adiciona filtros, ordenação e interações aos cartões da página de eventos. A opção de carregar mais eventos é demonstrativa e não busca conteúdo em um servidor.
- `js/gremio.js` cuida de animações e de uma janela com informações da equipe do grêmio.

Esses scripts podem alterar elementos já presentes no HTML ou exibir elementos de interface, mas não montam as páginas nem carregam as matérias de uma base de dados.

## Manutenção

As matérias e páginas são independentes. Para atualizar uma notícia, edite seu arquivo em `noticias/` e atualize também o cartão correspondente em `index.html`, se ele aparecer na página inicial. Ao criar ou mover páginas, confira os links, imagens e folhas de estilo, pois eles usam caminhos relativos.

O rodapé aparece repetido em diferentes arquivos HTML, e sua aparência é definida por folhas de estilo distintas. Isso significa que um ajuste pode precisar ser aplicado em mais de um lugar — um ponto importante ao investigar os problemas de rodapé mencionados no projeto.
