FROM node:18

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

# Build TypeScript (IMPORTANT)
RUN npm run build

EXPOSE 3001

# Run compiled JS (not TS)
CMD ["node", "dist/index.js"]