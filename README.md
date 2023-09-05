# order-service-rabbitmq

1. Order Service
   The Order Service is responsible for accepting customer orders and publishing events about these orders.
     - Created a new Spring Boot application.
     - Configured an H2 database for storing order information.
     - Created an Order entity and a corresponding repository to handle CRUD operations.
     - Created an OrderController with an endpoint for placing an order. This endpoint receives the order details, saves the order in the database, and publishes an "OrderPlaced" event.
     - Configured a RabbitMQ producer to publish the "OrderPlaced" event. The event contains relevant order details like OrderId, ProductId and Quantity.
