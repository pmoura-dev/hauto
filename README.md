# HAUTO - Home Automation System

Hauto is a simple home automation system.

## Architecture

HAUTO application core is composed currently by 4 components:

- **RabbitMQ** - A message broker that also acts as a MQTT broker. Responsible for delivering messages between services, and also communicate with the IOT devices.
- **API Gateway** - The API Gateway exposes the system's functionality to external applications. It receives requests via HTTP from the outside world and routes them to the appropriate microservices. It also provides a Websocket channel to that enables clients to listen for real time system changes.
- **TimescaleDB** - The systems's database.
- **Microservices** - The multiple microservices that handle the different functionalities of the system.
