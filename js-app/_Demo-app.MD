![image](https://user-images.githubusercontent.com/122154728/216611353-f2b822a8-6ec2-452b-940a-9f5cc37f4558.png)
```
docker network create mongo-network
```

![image](https://user-images.githubusercontent.com/122154728/216613856-a7f53ea2-cc5e-4970-bbfd-d646599535a6.png)


```
docker run -p 27017:27017 -d -e MONGO_INITDB_ROOT_USERNAME=admin  MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --network mongo-network mongo
```

```
docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net mongo-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb mongo-express
 ```
