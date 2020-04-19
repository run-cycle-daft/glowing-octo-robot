# glowing-octo-robot

Serverless Azure

## Getting Started

```
git clone [this]
```

### Prerequisites

>npm install -g lite-server

### Local CosmosDB MongoDB instance 

Dev set up
Windows 10 Home Ed with Visual Studio Code
If you don't have access to run the emulator in Docker and no access to Azure CosmosDB

- Install Visual Studio Code CosmosDB Plugin
- Download and install Microsoft CosmosDB Emulator
- Download and install MongoDB 4.2
-- Go through set up ensure its installed as a service
- Re-start Windows machine
- Start the Emulator with a data dir
-- Create a dir for the data, say `C:\monogodbdata`
-- Start the Empulator in that dir
```bash
cd C:\mongodbdata
"C:\Program Files\Azure Cosmos DB Emulator\Microsoft.Azure.Cosmos.Emulator.exe" /EnableMongoDbEndpoint
```
- In Visual Studio Code
-- Navigate to CosmosDB Plugin
-- Right click "Attach CosmosDB for MongoDB"
- Create your DB & a collection
-- Right click MongoDB connection "Create database...", give it a name (see in code)
-- Right click your database "Create collection...", give it a name (see in code)

### Example local func setting local.settings.json

```json
{
  "IsEncrypted": false,
  "Values": {
    "AzureWebJobsStorage": "",
    "FUNCTIONS_WORKER_RUNTIME": "node",
    "speakers_COSMOSDB": "mongodb://127.0.0.1:27017"
  },
  "Host" : {
    "LocalHttpPort": 7071,
    "CORS": "*"
  }
}
```

## Run locally

>cd frontend
>lite-server

>cd backend
>func start

## Running the tests

ToDo


## Deployment

ToDo

## Built With

* [Azure](https://aka.ms) - The platform

## License
This project is licensed under the MIT License

