FROM node:23-alpine

WORKDIR /backend-app
RUN apk update && apk add curl
COPY package.json ./
RUN npm install
COPY index.js ./
COPY .env ./

EXPOSE 5050


CMD [ "start" ]
ENTRYPOINT [ "npm" ]



# $ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres


# Image should be based on Node:22 
# Container start up command should be either “npm start” or “node index.js”
# Container need to expose its running service on 5050 port inside docker network.


# Step 2: Set Up and Run the Back-end
# Navigate to the backend directory:

# cd backend
# Install the required dependencies:

# npm install
# Create a .env file in the backend directory with the following content:

# DATABASE_URL=postgres://postgres:password@localhost:5432/mydatabase
# Make sure to replace password with your actual PostgreSQL password.

# Start the back-end server:

# npm start
# The back-end server should now be running at http://localhost:5000.