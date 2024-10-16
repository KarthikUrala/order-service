Order Service
The Order Service is a backend service that receives orders from the store-front and sends these orders to a RabbitMQ message queue. It enables decoupling of the order processing logic from the product service, allowing for more scalable and maintainable architecture.

Requirements
Node.js
npm
RabbitMQ
Setup Instructions
Update the package list:

sudo apt update
Install the NodeSource repository for Node.js 20: First, download and add the NodeSource repository for Node.js 20.x.

curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
Install Node.js and npm

sudo apt update
sudo apt install -y nodejs
Navigate to the order-service directory:

cd order-service
Install dependencies:

The service depends on several npm packages (such as express for the web server and amqplib for RabbitMQ communication). Install these dependencies using npm:

npm install
Run the service:

Once all dependencies are installed, start the service:

node index.js 
The service will be running on http://localhost:3000.

Testing
Before the service can send orders to RabbitMQ, make sure RabbitMQ is installed and running locally. If not, follow the setup instructions in the RabbitMQ documentation provided earlier.
Install the REST Client extension in VS Code to use .http files.
Use the provided test-order-service.http file to test the service.
