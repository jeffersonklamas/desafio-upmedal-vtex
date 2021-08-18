## Desafio VTEX IO - Desafio 3

O Objetivo é criar um template, com alguns pré requisitos:

### Para esta tela utilizar os componentes:

* **[Flex layout](https://vtex.io/docs/components/all/vtex.flex-layout@0.17.0/)** para criar as cores em CSS.
* Dar prioridade as páginas criada nos arquivos.jsonc colocando comentários dos blocos criados
* Utilizar o **[Slider layout](https://vtex.io/docs/app/vtex.slider-layout)** para mostrar os produtos em destaque 
* Criar um componente **[Tab Layout](https://vtex.io/docs/components/all/vtex.tab-layout@0.4.3/)** para separar os produtos por categoria.
* Criar um bloco de **[lista de produtos](https://vtex.io/docs/app/vtex.product-list@0.31.0/)**. ( Sugestão paginação por 8 itens da categoria)
* Criar **[Minicard](https://vtex.io/docs/components/content-blocks/vtex.minicart@2.60.0/)** para lista dos produtos no carrinho.
* Ao clicar no produto ir para tela com **[Product Summary](https://vtex.io/docs/components/all/vtex.product-summary@2.53.0/)**.

### Layout Mobile

* Criar um componente customizado para falar com suporte no whatsapp no rodapé.
    * utilizar o VTEX **[Componentes com React](https://vtex.io/docs/components/all/vtex.store-components@3.150.0/)** para criar o componente.
    * API https://www.convertte.com.br/gerador-link-whatsapp/.

* Criar um componente customizado para cadastrar leads (possíveis clientes prospectos).
    * Nome,
    * Email
    * Telefone
    * Este componente pode servir de isca digital , dando uma bonificação para o prospecto que preencher as informações da lead.
    * Utilizar o VTEX **[Componentes com React](https://vtex.io/docs/components/all/vtex.store-components@3.150.0/)** para criar o componente.
    * Sugestão de layout:
        * uma tela básica aparecendo uma caixa para o mesmo preencher o Nome Copleto, e-mail e telefone.
    * Mais sugestões para ajudar no layout:
    * **[Link 1](https://vtex.io/docs/getting-started/desenvolva-componentes-usando-vtex-io-e-react/5/)**.
    * https://vtex.io/docs/components/all/vtex.stack-layout@0.1.0/.

### AWS API Gateway

* Com o objetivo de armazenar as leads que o Vtex componente irá utilizar no React, criar uma API Gateway na AWS para colocar as informações - https://aws.amazon.com/pt/api-gateway/
* Um exemplo de arquivo API Gateway para estudo:
* https://github.com/awslabs/aws-api-gateway-developer-portal/blob/master/cloudformation/template.yaml
* https://github.com/mattpodolak/email-api-lambda
* https://github.com/amazon-archives/realworld-serverless-application/blob/master/backend/sam/app/api.template.yaml

### Opcional

Criar um item no adm do vtex para trazer o conteúdo das leads cadastradas na API Gateway AWS - Conteúdo do vídeo da aula 9 do curso.

A partir do template:

### Minimum Boilerplate Theme

The minimum Boilerplate Theme is basic store front model based on the VTEX IO Store Framework.

It should be used only when you want to start a new store theme without any pre-set configurations, as is the case with [Store Theme](https://github.com/vtex-apps/store-theme). 

While Store Theme gives developers a ready-to-go default store front structure, the Minimum Boilerplate Theme will enable you to build you store freely from scratch.

## Configuration

### Step 1 -  Basic setup

Access the VTEX IO [basic setup guide](https://vtex.io/docs/getting-started/build-stores-with-store-framework/1) and follow all the given steps. 

By the end of the setup, you should have the VTEX command line interface (Toolbelt) installed along with a developer workspace you can work in.

### Step 2 - Cloning the Minimum Boilerplate Theme repository

[Clone](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository) this repository to your local files to be able to effectively start working on it.

Then, access the repository's directory using your terminal. 

### Step 3 - Editing the `Manifest.json`

Once in the repository directory, it is time to edit the Minimum Boilerplate `manifest.json` file. 

Once you are in the file, you must replace the `vendor` and `account` values. `vendor` is the account name you are working on and `account` is anything you want to name your theme. For example:

```json
{
  "vendor": "storecomponents",
  "name": "my-test-theme",
}
```

### Step 4 -  Installing required apps

In order to use Store Framework and work on your store theme, it is needed to have both `vtex.store-sitemap` and `vtex.store` installed.

Run  `vtex list`  and check whether those apps are already installed. 

If they aren't, run the following command to install them: `vtex install vtex.store-sitemap vtex.store -f`

### Step 5 -  Uninstalling any existing theme

By running `vtex list`,  you can verify if any theme is installed.

It is common to already have a `vtex.store-theme`  installed when you start the store's front development process. 

Therefore, if you find it in the app's list, copy its name and use it together with the command `vtex uninstall`. For example:

```json
vtex uninstall vtex.store-theme
```

### Step 6- Run and preview your store

Then time has come to upload all the changes you made in your local files to the platform. For that, use the `vtex link` command. 

If the process runs without any errors, the following message will be displayed: `App linked successfully`. Then, run the `vtex browse` command to open a browser window having your linked store in it.

This will enable you to see the applied changes in real time, through the account and workspace in which you are working.
