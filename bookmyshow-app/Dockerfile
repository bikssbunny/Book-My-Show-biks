FROM node:latest
# Set working directory
WORKDIR /app
COPY package.json package-lock.json ./
# Force install a compatible PostCSS version to fix the issue
RUN npm install postcss@8.4.21 postcss-safe-parser@6.0.0 --legacy-peer-deps
#To Install dependencies
RUN npm i chokidar
RUN npm install
COPY . . 
EXPOSE 3000
ENV NODE_OPTIONS=--openssl-legacy-provider
ENV PORT=3000
