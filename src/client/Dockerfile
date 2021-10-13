FROM node:10 AS build
COPY package*.json ./
RUN npm install

FROM node:10 
WORKDIR app
COPY --from=build node_modules ./node_modules
COPY . .
CMD ["npm","start"]

EXPOSE 3000
