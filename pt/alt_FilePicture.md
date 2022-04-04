Primeiro cabeçalho | Segundo cabeçalho
--- | ---
Célula de Conteúdo | Célula de Conteúdo
Célula de Conteúdo | Célula de Conteúdo

Primeiro cabeçalho | Segundo cabeçalho
--- | ---
Célula de Conteúdo | Célula de Conteúdo
Célula de Conteúdo | Célula de Conteúdo

![Cidadela](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

Esquerda alinhada | Alinhado ao Centro | Alinhado à direita
:-- | :-: | --:
coluna 3 é | algum texto prolixo | **$ 1.600**
coluna 2 é | centrado | $ 12
listras de zebra | são legais | ~~$1~~

O Dillinger é um editor HTML5 Markdown habilitado para nuvem, pronto para dispositivos móveis, com armazenamento offline e alimentado por AngularJS.

- Digite algum Markdown à esquerda
- Veja HTML à direita
- Magia

# verdadeiro

- Import a HTML file and watch it magically convert to Markdown

Você também pode:

- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Arraste e solte markdown e arquivos HTML no Dillinger
- Exporte documentos como Markdown, HTML e PDF

Markdown is a lightweight markup language based on the formatting conventions that people naturally use in email.  As [John Gruber] writes on the [Markdown site][df1]

> O objetivo primordial do design para a sintaxe de formatação do Markdown é torná-lo o mais legível possível. A ideia é que um documento formatado pelo Markdown seja publicável como está, como texto simples, sem parecer que foi marcado com tags ou instruções de formatação.

Este texto que você vê aqui está *realmente* escrito em Markdown! Para ter uma ideia da sintaxe do Markdown, digite algum texto na janela esquerda e observe os resultados à direita.

### falso

Dillinger usa vários projetos de código aberto para funcionar corretamente:

- [AngularJS] - HTML aprimorado para aplicativos da web!
- [Ace Editor] - incrível editor de texto baseado na web
- [markdown-it] - analisador Markdown feito corretamente. Rápido e fácil de estender.
- [Twitter Bootstrap] - excelente padrão de interface do usuário para aplicativos da web modernos
- [node.js] - E/S com eventos para o back-end
- [Express] - framework de aplicativo de rede node.js rápido [@tjholowaychuk]
- [Gulp] - o sistema de compilação de streaming
- [Breakdance](https://breakdance.github.io/breakdance/) - conversor de HTML para Markdown
- [jQuery] - duh

E, claro, o próprio Dillinger é de código aberto com um [repositório público][dill] no GitHub.

### Instalação

![Ilos](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg)

O Dillinger requer que o [Node.js](https://nodejs.org/) v4+ seja executado.

Instale as dependências e devDependencies e inicie o servidor.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Para ambientes de produção...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plug-ins

Dillinger está atualmente estendido com os seguintes plugins. As instruções sobre como usá-los em seu próprio aplicativo estão no link abaixo.

Plugar | Leia-me
--- | ---
Dropbox | [plugins/dropbox/README.md][PlDb]
GitHubGenericName | [plugins/github/README.md][PlGh]
Google Drive | [plugins/googledrive/README.md][PlGd]
OneDrive | [plugins/onedrive/README.md][PlOd]
Médio | [plugins/medium/README.md][PlMe]
Google Analytics | [plugins/googleanalytics/README.md][PlGa]

### Desenvolvimento

## alt

As métricas que compõem o Core Web Vitals [evoluirão](#evolving-web-vitals) com o tempo. O conjunto atual para 2020 se concentra em três aspectos da experiência do usuário – *carregamento* , *interatividade* e *estabilidade visual* – e inclui as seguintes métricas

Quer contribuir? Excelente!

Dillinger usa Gulp + Webpack para desenvolvimento rápido. Faça uma alteração em seu arquivo e veja instantaneamente suas atualizações!

Abra seu Terminal favorito e execute esses comandos.

Primeira aba:

```sh
$ node app
```

Segunda guia:

```sh
$ gulp watch
```

(opcional) Terceiro:

```sh
$ karma test
```

#### Construindo para a fonte

Para liberação de produção:

```sh
$ gulp build --prod
```

Gerando arquivos zip pré-construídos para distribuição:

```sh
$ gulp build dist --prod
```

### Janela de encaixe

O Dillinger é muito fácil de instalar e implantar em um contêiner do Docker.

Por padrão, o Docker exporá a porta 8080, portanto, altere isso no Dockerfile, se necessário. Quando estiver pronto, basta usar o Dockerfile para construir a imagem.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

Isso criará a imagem do dillinger e extrairá as dependências necessárias. Certifique-se de trocar `${package.json.version}` pela versão real do Dillinger.

Uma vez feito, execute a imagem do Docker e mapeie a porta para o que você desejar em seu host. Neste exemplo, simplesmente mapeamos a porta 8000 do host para a porta 8080 do Docker (ou qualquer porta exposta no Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verifique a implantação navegando até o endereço do servidor em seu navegador preferido.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

Veja [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### Todos
