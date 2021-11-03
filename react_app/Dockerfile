FROM node:17-alpine
RUN apk -U upgrade
RUN apk add --update --no-cache bash
RUN apk add --update --no-cache curl
RUN curl -f https://get.pnpm.io/v6.16.js | node - add --global pnpm
WORKDIR /app
COPY package.* .
RUN pnpm install
COPY . .
RUN pnpm build
EXPOSE 3000
EXPOSE 5000
CMD ["pnpm", "serve"]

