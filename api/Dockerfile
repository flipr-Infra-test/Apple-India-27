FROM node:24-alpine AS base
WORKDIR /app
COPY package*.json ./
RUN npm ci --prefer-offline --no-audit || npm install
COPY . .
RUN if npm run | grep -q "build"; then npm run build; fi
EXPOSE 3000
CMD ["npm", "start"]
