# General architecture

### Facebook messenger -> AWS -> Next-Level-Education -> AWS -> Facebook messenger

1. Facebook messenger receives a message from the user. The message is sent to AWS (API Gateway -> Lambda -> Serverless stuff).
2. Next-Level-Education receives the message and processes it.
3. Next-Level-Education calls any functions that are required to be called (save name to database, save occupation to database, see below). The database is DynamoDB.
4. Next-Level-Education sends a message back to Facebook Messenger

## High-level design diagram
<p align="center"><img src="/img/chatbot_architecture.png" alt="High-level design diagram"/></p>

## Low-level design diagram (non-chronological)
<p align="center"><img src="/img/low_level_diagram.jpg" alt="Low-level design diagram"/></p>

## Sequence diagram
<p align="center"><img src="/img/sequence_diagram.jpg" alt="Sequence diagram"/></p>

