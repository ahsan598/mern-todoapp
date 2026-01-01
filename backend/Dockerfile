# ======================================================
# Stage 1: Build Stage
# ======================================================
FROM node:24-alpine3.23 AS builder

# Set the working directory in the container
WORKDIR /app

# Copy the package.json & package-lock.json files
COPY package*.json ./

# Install the application's dependencies inside the container
RUN npm ci --only=production

# ======================================================
# Stage 2: Final Stage
# ======================================================
FROM node:24-alpine3.23
WORKDIR /app

# Set production environment
ENV NODE_ENV=production

# Non-root user setup (Node image has a 'node' user by default)
USER node

# Copy only necessary artifacts from builder stage
COPY --from=builder --chown=node:node /app/node_modules ./node_modules
COPY --chown=node:node . .

# Expose Port to the container
EXPOSE 8080

# Specify the command to run when the container starts
CMD [ "node", "index.js" ]
