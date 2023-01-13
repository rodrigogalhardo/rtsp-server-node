# rtsp stream teste

Para usar com o client baixe esse repositorio:
> https://github.com/rodrigogalhardo/rtsp-client-js.git

Para rodar a aplicação sem docker:

1 - Na pasta servers/socket-server executar os seguintes comandos:

a) > yarn install # para instalar as dependencias.
b) > yarn run start # para rodar o server rtsp node.

2 - Na pasta client possui 2 htmls:

a) index.html que corresponde ao item 1) a e b. 
Para executar basta abrir uma pagina html no browser e colocar o link do RTSP desejado. 

b) index2.html, é uma versão para executar com o docker:

docker pull kavyesh/node-rtsp-ws:1.0

Ps: URL=rtsp:// put the URL into docker command.

Ex: (funciona):

docker run -p 9999:9999 -e URL=rtsp://wowzaec2demo.streamlock.net/vod/mp4:BigBuckBunny_115k.mp4 -e WS_PORT=9999 kavyesh/node-rtsp-ws:1.0

Basta executar com um web server a pagina index2 da seguinte forma:

python -m http.server, conforme abaixo:

python3 -m http.server
Serving HTTP on :: port 8000 (http://[::]:8000/) ...

em seguida chamar a porta 8000