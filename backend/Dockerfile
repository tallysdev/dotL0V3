FROM node:18
WORKDIR /app
COPY package.json package-lock.json ./
COPY package*.json ./
COPY prisma ./prisma
COPY .env ./
COPY tsconfig.json ./
RUN npm install
COPY . .
RUN npx prisma generate
EXPOSE 5432
