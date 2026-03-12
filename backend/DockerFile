# =============================================
# Dockerfile - Backend (NestJS)
# =============================================

# Usa a mesma base do frontend: Node.js LTS em Alpine
FROM node:lts-alpine

# Define o diretório de trabalho
WORKDIR /app

# Copia os arquivos de dependências primeiro (otimização de cache)
COPY package*.json ./

# Instala as dependências
# O NestJS usa o CLI para rodar em modo watch (hot-reload)
RUN npm install

# Copia o código-fonte
# Assim como o frontend, em dev o volume sobrescreve esses arquivos
COPY . .

# Expõe a porta padrão do NestJS
EXPOSE 3000

# Inicia o NestJS em modo de desenvolvimento com hot-reload
# O flag --watch faz o NestJS reiniciar automaticamente ao detectar mudanças
CMD ["npm", "run", "start:dev"]