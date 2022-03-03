# ZAKI NIGHT
 > Zakinight é um sistema de alto desempenho desenvolvido com JavaScript para criar um bot para WhatsApp, suporte para criar qualquer interação, como atendimento ao cliente, envio de mídia, reconhecimento de sentenças baseado em inteligência artificial e todos os tipos de arquitetura de design para WhatsApp.

## Comece agora usando a api do Venom-bot

É uma API alternativa de alto desempenho para o whatzapp, você pode enviar mensagens de texto, arquivos, imagens, vídeos e muito mais.

Lembre-se, a API foi desenvolvida em uma plataforma chamada RESTful Web services, fornecendo interoperabilidade entre sistemas de computador na Internet.

Ele usa um conjunto de operações bem definidas que se aplicam a todos os recursos de informação: o próprio HTTP define um pequeno conjunto de operações, sendo o mais importante POST, GET, PUT e DELETE.

Use-o em sua linguagem favorita como PHP, Python, C# e outros. desde que seu idioma seja suportado com o protocolo HTTP, você economizará tempo e dinheiro. você não precisa saber como o Venom funciona, temos a documentação completa da API, de forma profissional!


## Funções do Zaki Night

|                                                               |   |
|---------------------------------------------------------------|---|
| 🚻 Atualização automática de QR  | ✔ |
| 📁 Enviar **texto, imagem, vídeo, áudio e docs** | ✔ |
| 👥 Obtenha **contatos, chats, grupos, membros do grupo, Lista de blocos** | ✔ |
| 📞 Envie contatos | ✔ |
| Enviar botões | ✔ |
| Envie adesivos | ✔ |
| Envie adesivos GIF | ✔ |
| Sessões múltiplas | ✔ |
| ⏩ Mensagens de encaminhamento | ✔ |
| 📥 Receba mensagens  | ✔ |
| 👤 inserir seção de usuário | ✔ |
| 📍 Envie localização!! | ✔ |
|**e muito mais** | ✔ |


```
## Sessão de status de retorno de chamada

Obtém o retorno se a sessão estiver 'isLogged' ou 'notLogged' ou 'browserClose' ou 'qrReadSuccess' ou 'qrReadFail' ou 'autocloseCalled' ou 'desconectadoMobilizar' ou 'excluirToken' ou 'chats Disponível' ou dispositivo 'Não Conectado' ou 'serverWssNotConnected' ou 'noOpenBrowser' ou 'Criar sessão wss retornar servidor de caso "serverClose" para fechar'


| Status                  | Condição                                                                                                                                             
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
