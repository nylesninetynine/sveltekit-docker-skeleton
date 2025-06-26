# Stage 1: Build
FROM node:20 AS builder
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build

# Stage 2: Run
FROM node:20
WORKDIR /app
COPY --from=builder /app ./
RUN npm install --omit=dev
CMD ["node", "build"]