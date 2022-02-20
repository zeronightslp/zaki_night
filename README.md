# zaki_night
 > Zakinight é um sistema de alto desempenho desenvolvido com JavaScript para criar um bot para WhatsApp, suporte para criar qualquer interação, como atendimento ao cliente, envio de mídia, reconhecimento de sentenças baseado em inteligência artificial e todos os tipos de arquitetura de design para WhatsApp.

## Comece rápido e fácil! API oficial!

É uma API alternativa de alto desempenho para o whatzapp, você pode enviar mensagens de texto, arquivos, imagens, vídeos e muito mais.

Lembre-se, a API foi desenvolvida em uma plataforma chamada RESTful Web services, fornecendo interoperabilidade entre sistemas de computador na Internet.

Ele usa um conjunto de operações bem definidas que se aplicam a todos os recursos de informação: o próprio HTTP define um pequeno conjunto de operações, sendo o mais importante POST, GET, PUT e DELETE.

Use-o em sua linguagem favorita como PHP, Python, C# e outros. desde que seu idioma seja suportado com o protocolo HTTP, você economizará tempo e dinheiro. você não precisa saber como o Venom funciona, temos a documentação completa da API, de forma profissional!


## Funções do Zaki Night

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

```javascript
// Init sales whatsapp bot
venom.create('sales').then((salesClient) => {...});
// Init  suporte whatsapp bot
venom.create('support').then((supportClient) => {...});
```

<br>

## Opcionais criar parâmetros

O terceiro parâmetro do método Zaki 'create()' pode ter os seguintes parâmetros opcionais:

Se você estiver usando o servidor 'Linux' não se esqueça de passar o '-agente do usuário' args
[Parâmetros originais no browserArgs] (https://github.com/orkestral/venom/blob/master/src/config/puppeteer.config.ts)

```javascript
const venom = require('zaki-night');
venom
  .create(
    //session
    'sessionName', /Passe o nome do cliente que deseja iniciar o bot
    //catchQR
    (base64Qrimg, asciiQR, attempts, urlCode) => {
      console.log('Number of attempts to read the qrcode: ', attempts);
      console.log('Terminal qrcode: ', asciiQR);
      console.log('base64 image string qrcode: ', base64Qrimg);
      console.log('urlCode (data-ref): ', urlCode);
    },
    // statusFind
    (statusSession, session) => {
      console.log('Status Session: ', statusSession); //return isLogged || notLogged || browserClose || qrReadSuccess || qrReadFail || autocloseCalled || desconnectedMobile || deleteToken || chatsAvailable || deviceNotConnected || serverWssNotConnected || noOpenBrowser
      // Criar sessão wss retornar servidor de caso "serverClose" para fechar
      console.log('Session name: ', session);
    },
    // opcões
    {
      multidevice: false, //para versão não uso multidevice falso(default: true)
      folderNameToken: 'tokens', ///nome da pasta ao salvar tokens
      mkdirFolderToken: '', /folder directory tokens, apenas dentro da pasta zaki, exemplo: { mkdirFolderToken: '/node_modules', } //salvará a pasta de tokens no diretório node_modules
      headless: true, //chrome sem cabeça
      devtools: false, //  Abrir devtools por padrão
      useChrome: true, // Se falso usará a ocorrência de Chrome
      debug: false, //Abre uma sessão de depuração
      logQR: true, // Logs QR automaticamente no terminal
      browserWS: '', //se você quiser usar browserWSEndpoint
      browserArgs: [''], /Parâmetros originais ---Parameters a serem adicionados na instância do navegador chrome
      puppeteerOptions: {}, // Será passado para puppeteer.launch
      disableSpins: true, // Desativará a animação Spinnies, útil para contêineres (docker) para um melhor log
      disableWelcome: true, // Desativará a mensagem de boas-vindas que aparece no início
      updatesLog: true, // Logs atualizações de informações automaticamente no terminal
      autoClose: 60000, //Fecha automaticamente o veneno-bot somente ao digitalizar o código QR (padrão de 60 segundos, se você quiser desligá-lo, atribuir 0 ou false)
      createPathFileToken: false, //  cria uma pasta ao inserir um objeto no navegador do cliente, para trabalhar é necessário passar os parâmetros na função criar browserSessionToken
      chromiumVersion: '818858', //Versão do navegador que será usado. As cordas de revisão podem ser obtidas a partir de omahaproxy.appspot.com.
      addProxy: [''], // Adicionar exemple servidor proxy : [e1.p.webshare.io:01, e1.p.webshare.io:01]
      userProxy: '', // Nome de usuário de login proxy
      userPass: '' // Proxy senha
    },
    // BrowserSessionToken
    // Para receber o token do cliente, use a função aguarde clinet.getSessionTokenBrowser()
    {
      WABrowserId: '"UnXjH....."',
      WASecretBundle:
        '{"key":"+i/nRgWJ....","encKey":"kGdMR5t....","macKey":"+i/nRgW...."}',
      WAToken1: '"0i8...."',
      WAToken2: '"1@lPpzwC...."'
 },
    // BrowserInstance
    (browser, waPage) => {
      console.log('Browser PID:', browser.process().pid);
      waPage.screenshot({ path: 'screenshot.png' });
    }
  )
  .then((client) => {
    start(client);
  })
  .catch((erro) => {
    console.log(erro);
  });
```
## Sessão de status de retorno de chamada

Obtém o retorno se a sessão estiver 'isLogged' ou 'notLogged' ou 'browserClose' ou 'qrReadSuccess' ou 'qrReadFail' ou 'autocloseCalled' ou 'desconectadoMobilizar' ou 'excluirToken' ou 'chats Disponível' ou dispositivo 'Não Conectado' ou 'serverWssNotConnected' ou 'noOpenBrowser' ou 'Criar sessão wss retornar servidor de caso "serverClose" para fechar'


| Status                  | Condição                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `isLogged`              | Quando o usuário já está logado no navegador                                                                                                  |
| `notLogged`             | Quando o usuário não está conectado ao navegador, é necessário digitalizar o código QR através do celular na opção WhatsApp Web                    
| `browserClose`          | Se o navegador estiver fechado, este parâmetro será devolvido                                                                                    
| `qrReadSuccess`         | Se o usuário não estiver logado, o código QR será repassado no terminal, uma chamada de retorno será devolvida. Após a leitura correta pelo celular este parâmetro é devolvido |
| `qrReadFail`            |  Se o navegador parar quando a varredura de código QR estiver em andamento, este parâmetro será devolvido                                          | 
| `autocloseCalled`       | O navegador foi fechado usando o comando autoClose                                                                                                 |
| `desconnectedMobile`    | Cliente se desconectou a | móveis                                                                                                                  |
| `serverClose`           |  Cliente se desconectou ao WSS                                                                                                                     |
| `deleteToken`           | Se você passar verdadeiro dentro da função  `client.getSessionTokenBrowser(true)`                                                                  |
| `chatsAvailable`        |Quando Zaki estiver conectado à lista de bate-papo                                                                                                  |
| `deviceNotConnected`    | Chat não disponível porque o telefone está desconectado `(Trying to connect to the phone)`                                                         |
| `serverWssNotConnected` | O endereço wss não foi encontrado!                                                                                                                 |
| `noOpenBrowser`         | INão foi encontrado no navegador, ou algum comando está faltando em args                                                                           |

```javascript
const zaki = require('zaki-night');
Zaki
  .create(
    'sessionName',
    undefined,
    (statusSession, session) => {
      console.log('Status Session: ', statusSession);
     eturn isLogged || || não-|| browserClose || qrLelesuccess || qrReadFail || autocloseCalled || || desconectado doMobile deleteToken || chats Disponíveis || dispositivoNconectado || servidorWssNotConectado || noOpenBrowser
      // Criar sessão wss retornar servidor de caso "serverClose" para fechar     
     console.log('Session name: ', session);
    },
    {
      multidevice: false // para versão não uso multidevice falso.(default: true)
    }
  )
  .then((client) => {
    start(client);
  })
  .catch((erro) => {
    console.log(erro);
  });
```
## QR Code exportador

Por código QR padrão aparecerá no terminal. Se você precisa passar o QR
em outro lugar aquis como:

```javascript
const fs = require('fs');
const zaki = require('zaki-night');
Zaki
  .create(
    'sessionName',
    (base64Qr, asciiQR, attempts, urlCode) => {
      console.log(asciiQR); // Opcional para registrar o QR no terminal
      var matches = base64Qr.match(/^data:([A-Za-z-+\/]+);base64,(.+)$/),
        response = {};
      if (matches.length !== 3) {
        return new Error('Invalid input string');
      }
      response.type = matches[1];
      response.data = new Buffer.from(matches[2], 'base64');
      var imageBuffer = response;
      require('fs').writeFile(
        'out.png',
        imageBuffer['data'],
        'binary',
        function (err) {
          if (err != null) {
            console.log(err);
          }
        }
      );
    },
    undefined,
    { logQR: false }
  )
  .then((client) => {
    start(client);
  })
  .catch((erro) => {
    console.log(erro);
  });
```
## Baixar arquivos

Puppeteer cuida do download do arquivo. A descriptografia está sendo feita como
o mais rápido possível (supera métodos nativos). Suporta arquivos grandes!

```javascript
import fs = require('fs');
import mime = require('mime-types');
client.onMessage( async (message) => {
  if (message.isMedia === true || message.isMMS === true) {
    const buffer = await client.decryptFile(message);
    // Neste ponto você pode fazer o que quiser com o buffer
    // Provavelmente você quer escrevê-lo em um arquivo
    const fileName = `some-file-name.${mime.extension(message.mimetype)}`;
    await fs.writeFile(fileName, buffer, (err) => {
      ...
    });
  }
});
```

