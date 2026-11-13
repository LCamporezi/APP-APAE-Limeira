# APP APAE Limeira

Site estático da APAE Limeira, em HTML, CSS e JavaScript, preparado para publicação na Vercel.

## Estrutura

```text
.
├── public/
│   ├── index.html      # Página inicial do site
│   └── assets/         # Imagens, arquivos CSS, JavaScript e outros recursos
├── .gitignore
├── README.md
└── vercel.json         # Configuração de publicação
```

## Atualizar o HTML

1. Edite ou substitua `public/index.html` pelo HTML que deseja publicar.
2. Coloque arquivos adicionais em `public/assets/`.
3. Referencie esses arquivos no HTML, por exemplo: `/assets/logo.png`, `/assets/style.css` ou `/assets/app.js`.
4. Faça commit e envie as alterações para o GitHub.

O HTML atual mantém o CSS e o JavaScript no próprio arquivo e o logotipo incorporado.

## Visualizar localmente

Com Python 3 instalado, execute na raiz do repositório:

```sh
python3 -m http.server 8000 --directory public
```

Acesse <http://localhost:8000>. Para encerrar, pressione `Ctrl+C`.

## Publicar na Vercel

1. Acesse <https://vercel.com/new> e entre com sua conta.
2. Conecte o GitHub e autorize o acesso ao repositório `LCamporezi/APP-APAE-Limeira`.
3. Importe o repositório e mantenha **Root Directory** na raiz (`./`).
4. Confira as configurações:

   | Opção | Valor |
   | --- | --- |
   | Framework Preset | Other |
   | Build Command | Sem comando |
   | Install Command | Sem comando |
   | Output Directory | `public` |
   | Production Branch | `main` |

5. Clique em **Deploy**. A Vercel fornecerá o endereço público do site.

O arquivo `vercel.json` define a pasta de saída e dispensa instalação de dependências e compilação. Não é necessário configurar variáveis de ambiente para servir o HTML atual.

Depois de conectar o projeto, cada push na branch `main` gera uma nova publicação de produção. Pull requests geram prévias conforme as configurações da integração GitHub/Vercel.

Para usar um domínio próprio, abra **Settings → Domains** no projeto da Vercel e siga as instruções de DNS exibidas.

## Funcionamento

A publicação serve arquivos estáticos. Integrações externas e formulários seguem o comportamento definido no HTML; a hospedagem não adiciona um backend ou banco de dados.
