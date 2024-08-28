# 🌐 Protocolo HTTP - Visão Geral

## 1. Conhecendo o HTTP

### ❓ O que é HTTP?
HTTP (Hypertext Transfer Protocol) é um protocolo de comunicação usado para transferir dados na web, como páginas HTML, imagens e vídeos. Ele permite que navegadores (clientes) e servidores web se comuniquem, sendo essencial para a navegação na internet.

### 🛠️ Arquitetura do HTTP
A arquitetura HTTP segue um modelo cliente-servidor:
- **Cliente (navegador)**: Envia uma requisição HTTP ao servidor.
- **Servidor (backend)**: Processa a solicitação e responde com os dados requisitados (ex: página web).

### 📚 Camadas da Arquitetura da Internet
A internet é dividida em várias camadas:
1. Física
2. Enlace de Dados
3. Rede
4. Transporte
5. Aplicação

O HTTP opera na camada de aplicação, que define como os dados são trocados entre aplicações (como navegadores e servidores).

### 🔄 O que é um Protocolo?
Um protocolo é um conjunto de regras que define como os dispositivos se comunicam. O HTTP define essas regras para garantir uma "conversa" padronizada entre cliente e servidor.

### 🔄 Protocolo Alternativo ao HTTP: P2P
O protocolo **P2P (Peer-to-Peer)** é uma alternativa ao HTTP, onde todos os dispositivos conectados (peers) atuam como clientes e servidores ao mesmo tempo, compartilhando recursos diretamente entre si. Diferente do modelo cliente-servidor do HTTP, o P2P não depende de um servidor central.

## 2. 🌍 Aprendendo sobre URLs

### 🖇️ O que é uma URL?
Uma URL (Uniform Resource Locator) é o endereço usado para acessar recursos na web. Ela é composta por:
- **Protocolo**: `http://` ou `https://`
- **Domínio**: `www.exemplo.com`
- **Caminho**: `/pasta/pagina.html`
- **Parâmetros**: `?id=123`

### 🆔 Diferença entre URI e URL
Uma URI (Uniform Resource Identifier) é um identificador genérico de um recurso na web, podendo ser um nome (URN) ou um endereço (URL). Uma URL é uma URI que especifica a localização exata de um recurso.

### 🔌 Portas Padrão
- **HTTP**: Porta 80
- **HTTPS**: Porta 443
- **Portas Livres**: 1024 a 49151 estão disponíveis para uso personalizado.

### 🌐 Como funciona o DNS?
O DNS (Domain Name System) traduz nomes de domínio em endereços IP. Quando você digita um domínio, o DNS encontra o IP correspondente para conectar ao servidor correto.

### ✅ Importância de URLs Fáceis
URLs fáceis de entender são importantes porque:
- Facilita a memorização.
- Melhora a experiência do usuário.
- Ajuda no SEO (otimização para motores de busca).
- Transmite confiança e clareza sobre o conteúdo.

## 3. 🔍 Inspecionando o Protocolo HTTP

### 📨 Formato das Mensagens HTTP
As mensagens HTTP podem ser:
- **Requisição (cliente)**:
  - Linha de requisição: Método (GET, POST), URL, versão HTTP.
  - Cabeçalhos: Metadados como tipo de conteúdo.
  - Corpo (opcional): Dados enviados, como formulários.
- **Resposta (servidor)**:
  - Linha de status: Versão HTTP, código de status (ex: 200 OK).
  - Cabeçalhos: Informações adicionais, como tipo de conteúdo.
  - Corpo: Dados retornados, como HTML.

### ✉️ Principais Métodos HTTP
- **GET**: Solicita visualização de um recurso (ex: página web).
- **POST**: Envia dados ao servidor (ex: formulário).
- **PUT**: Atualiza um recurso existente.
- **DELETE**: Remove um recurso.
- **PATCH**: Aplica modificações parciais a um recurso.
- **HEAD**: Solicita apenas os cabeçalhos de um recurso.

### 📦 O que significa "stateless"?
Um servidor HTTP é "stateless" porque não mantém informações sobre interações anteriores com o cliente. Cada requisição é independente.

### 🍪 Sessões e Cookies
- **Cookies**: Arquivos armazenados no navegador, guardam dados como identificadores de sessão.
- **Sessões**: Guardam informações no servidor, associadas a um usuário através de um cookie.

### 🔢 Códigos de Status HTTP
- **200 (OK)**: Requisição bem-sucedida.
- **201 (Created)**: Recurso criado com sucesso.
- **401 (Unauthorized)**: Autenticação necessária ou falha.
- **403 (Forbidden)**: Acesso ao recurso proibido.
- **404 (Not Found)**: Recurso não encontrado.
- **500 (Internal Server Error)**: Erro interno no servidor.

## 4. 🔒 Protegendo a Web com HTTPS

### 🔐 O que é HTTPS?
HTTPS (Hypertext Transfer Protocol Secure) é a versão segura do HTTP. Ele usa criptografia para proteger os dados transmitidos entre cliente e servidor.

### 🛡️ Papel do TLS no HTTPS
O **TLS (Transport Layer Security)** criptografa os dados, autenticando o servidor para evitar ataques como interceptação e manipulação de dados.

### 🔑 Criptografia Assimétrica no HTTPS
Na criptografia assimétrica, o servidor usa uma chave pública para criptografar os dados, e uma chave privada para descriptografá-los. Isso garante que apenas o servidor possa ler os dados.

### 🔄 Criptografia Simétrica vs. Assimétrica
- **Simétrica**: Usa uma única chave para criptografar e descriptografar. É mais rápida.
- **Assimétrica**: Usa um par de chaves (pública e privada). É mais segura, mas mais lenta.

## 5. 🎛️ Controlando o HTTP

### 🔄 Diferença entre GET e POST
- **GET**: Parâmetros enviados na URL como query parameters.
- **POST**: Parâmetros enviados no corpo da requisição.

### ❓ O que são Query Parameters?
São dados anexados à URL após o `?`, usados para enviar informações ao servidor (ex: filtros de pesquisa).

### 📤 Como os dados são enviados no POST?
No **POST**, os dados são transmitidos no corpo da requisição, mantendo-os ocultos da URL.

### 🚫 Limitações do GET
- **Tamanho limitado da URL**.
- **Visibilidade dos parâmetros**.
- **Cache**: Pode armazenar dados sensíveis.

### ✅ Quando usar POST?
- **Dados sensíveis**.
- **Grandes quantidades de dados**.
- **Alterações no servidor**.
- **Evitar cache**.

## 6. 🚀 Conhecendo as Evoluções do HTTP

### 🚀 Melhorias do HTTP/2
- **Multiplexação**: Várias requisições simultâneas.
- **Compressão de cabeçalhos**: Reduz o tamanho das mensagens.
- **Server Push**: Envio proativo de recursos.
- **Protocolo binário**: Mais eficiente.
- **Melhor performance**: Reduz latência e aumenta velocidade.

### 🔄 Multiplexação no HTTP/2
Permite múltiplas requisições e respostas ao mesmo tempo, através de uma única conexão, tornando a comunicação mais rápida.

### 🗜️ Compressão de Cabeçalhos no HTTP/2
Usa o algoritmo HPACK para diminuir o tamanho dos cabeçalhos, acelerando a troca de dados e economizando largura de banda.

### 🌍 HTTP/3 e QUIC
O **HTTP/3** usa o protocolo **QUIC** baseado em UDP, trazendo:
- **Conexões mais rápidas**.
- **Melhor desempenho em redes instáveis**.
- **Sem bloqueio de linha de frente**.
- **Segurança integrada com TLS 1.3**.
