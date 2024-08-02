FROM node:19.0.0-slim
WORKDIR /usr/app

ONBUILD COPY package*.json ./

ONBUILD RUN npm ci

ONBUILD COPY . ./

# Build for production
ONBUILD RUN npm run build:prod && \
    npm prune --production