# zaki_night
 > Zakinight é um sistema de alto desempenho desenvolvido com JavaScript para criar um bot para WhatsApp, suporte para criar qualquer interação, como atendimento ao cliente, envio de mídia, reconhecimento de sentenças baseado em inteligência artificial e todos os tipos de arquitetura de design para WhatsApp.

## Comece rápido e fácil! API oficial!

É uma API alternativa de alto desempenho para o whatzapp, você pode enviar mensagens de texto, arquivos, imagens, vídeos e muito mais.

Lembre-se, a API foi desenvolvida em uma plataforma chamada RESTful Web services, fornecendo interoperabilidade entre sistemas de computador na Internet.

Ele usa um conjunto de operações bem definidas que se aplicam a todos os recursos de informação: o próprio HTTP define um pequeno conjunto de operações, sendo o mais importante POST, GET, PUT e DELETE.

Use-o em sua linguagem favorita como PHP, Python, C# e outros. desde que seu idioma seja suportado com o protocolo HTTP, você economizará tempo e dinheiro. você não precisa saber como o Venom funciona, temos a documentação completa da API, de forma profissional!

## Pegue a api do venom oficial da API ! Entre em contato conosco!

<a target="_blank" href="https://web.whatsapp.com/send?phone=556181590153&text=I%20want%20access%20to%20API%20Venom" target="_blank"><img title="whatzapp" height="100" width="375" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/WhatsApp_logo.svg/2000px-WhatsApp_logo.svg.png"></a>

## Suporte do grupo Venom gratuitamente no Telegram

<a target="_blank" href="https://t.me/joinchat/G8wxNXidWBo1ZDYx" target="_blank"><img title="Telegram" height="100" width="375" src="https://user-images.githubusercontent.com/66584466/117182238-7d1d8980-adac-11eb-9a70-e32f90c3d4e5.png"></a>

## Conheça os Superchats
<br>
<a href='https://github.com/orkestral/superchats'><img src='https://github.com/orkestral/superchats/raw/main/img/superchats.png' altura='60' alt='SuperChats' aria-label='https://github.com/orkestral/superchats' /></a>
<br>
<br>

**SuperChats** é uma biblioteca premium com recursos exclusivos que controlam as funções do Whatsapp com soquete.
Com superchats você pode construir bots de serviço, chats multiserviços ou qualquer sistema que use o Whatsapp

**Superchats** é uma versão premium do **Venom**, com recursos exclusivos e suporte para empresas e desenvolvedores em todo o mundo
<br>
<a href='https://github.com/orkestral/superchats'>https://github.com/orkestral/superchats</a>

## Compre uma licença Superchats

O valor da licença é de $30 dólares mensais, para adquirir contato no whatsapp clicando na imagem abaixo !!

<a target="_blank" href="https://web.whatsapp.com/send?phone=556181590153&text=I%20want%20to%20buy%201%20license" target="_blank"><img title="whatzapp" height="100" width="375" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/WhatsApp_logo.svg/2000px-WhatsApp_logo.svg.png"></a>

## 🕷🕷 Funções do Zaki Night

|                                                               |   |
|---------------------------------------------------------------|---|
| 🚻 | de atualização automática de QR ✔ |
| 📁 Enviar **texto, imagem, vídeo, áudio e docs** | ✔ |
| 👥 Obtenha **contatos, chats, grupos, membros do grupo, Lista de blocos** | ✔ |
| 📞 Envie contatos | ✔ |
| Enviar botões | ✔ |
| Envie adesivos | ✔ |
| Envie adesivos GIF | ✔ |
| Sessões múltiplas | ✔ |
| ⏩ Mensagens de encaminhamento | ✔ |
| 📥 Receba | mensagens ✔ |
| 👤 inserir seção de usuário | ✔ |
| 📍 Envie localização!! | ✔ |
| 🕸🕸 **e muito mais** | ✔ |

## Instalação

Instalando o repositório atual "você pode baixar a versão beta do repositório atual!"

'''bash
> npm i github:zeronightk/zakinight
```
## Começar Multidevice e Normal

''javascript
// Suporta ES6
// importação { criar, Whatsapp } de 'zaki-night';
zaki const  = necessário ('zaki-night');

zaki
  .create({
    session: 'session-name', //nome da sessão
    multidevice: false // para versão não uso multidevice falso.(default: true)
  })
  .then((client) => start(client))
  .catch((erro) => {
    console.log(erro);
  });
function start(client) {
  client.onMessage((message) => {
    if (message.body === 'Hi' && message.isGroupMsg === false) {
      client
        .sendText(message.from, 'Bem vindo zaki')
        .then((result) => {
          console.log('Result: ', result); ///retorno sucesso de objeto
        })
        .catch((erro) => {
          console.error('Error when sending: ', erro); //erro de objeto de retorno
        });
    }
  });
}
```
###### Depois de executar a função 'create()', **venom** criará uma instância da web do whatsapp. Se você não estiver logado, imprimirá um código QR no terminal. Escaneie com seu telefone e você está pronto para ir!

##### Zaki se lembrará da sessão para que não haja necessidade de autenticar todas as vezes.

##### As sessões de múltiplos podem ser criadas ao mesmo tempo, escolhendo um nome de sessão para 'create()':

mais informações acesse o site do venom bot 
https://github.com/orkestral/venom/blob/master/README.md
