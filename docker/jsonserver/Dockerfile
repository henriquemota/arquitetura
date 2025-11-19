 # imagem oficial do Node.js na tag "lts-alpine"
FROM node:lts-alpine

# Instala pacotes do sistema sem cache para não aumentar a camada
# adiciona tzdata (fuso horário) e remove cache do apk
RUN apk add --no-cache tzdata
# Define a variável de ambiente TZ para ajustar o fuso horário dentro do container
# define o timezone para Fortaleza (útil se o app precisa de horário local)
ENV TZ="America/Fortaleza"

# Define o diretório de trabalho dentro do container
# todas as instruções seguintes (COPY, RUN, CMD) serão relativas a /app
WORKDIR /app
# Instala globalmente o json-server via npm
# instala a ferramenta que serve um JSON como API REST
RUN npm install -g json-server

# Expõe a porta na qual o json-server irá escutar
# documentação/metadata: informa que o container usa a porta 3000
EXPOSE 3000

# Comando padrão executado quando o container inicia
# inicia o servidor observando data.json e aceitando conexões externas
CMD ["json-server", "--watch", "data.json", "--host", "0.0.0.0"]