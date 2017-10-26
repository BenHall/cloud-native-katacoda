Now that Catalog and Inventory services are up and running, start the API Gateway service:

`mvn vertx:run`{{execute T1}}

> You will see the following exception in the logs: `java.io.FileNotFoundException: .../kubernetes.io/serviceaccount/token`
> 
> This is expected and is the result of Vert.x trying to import services form OpenShift. Since you are 
> running the API Gateway on your local machine, the lookup fails and falls back to the local service 
> lookup. It's all good!

Now you can test the API Gateway by hitting the **/api/products** endpoint using **curl**

`curl http://localhost:8080/api/products`{{execute T4}}

You should see a JSON response like:
```
[{
  "itemId" : "329299",
  "name" : "Red Fedora",
  "desc" : "Official Red Hat Fedora",
  "price" : 34.99,
  "availability" : {
    "quantity" : 35
  }
...
```

Note that the JSON response aggregates responses fro Catalog and Inventory services and 
the inventory info for each product is available within the same JSON object.

Stop all services by pressing **CTRL-C** in the terminal windows.