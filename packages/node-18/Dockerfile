FROM node:18.20.3-slim
WORKDIR /usr/app

ONBUILD COPY package*.json ./

ONBUILD RUN npm ci

ONBUILD COPY . ./

# Build for production
ONBUILD RUN npm run build:prod && \
    npm prune --production