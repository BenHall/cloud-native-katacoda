Using Spring Boot maven plugin, you can conveniently run the application locally and test the endpoint.

`mvn spring-boot:run`{{execute}}

When you see **Started CatalogApplication** in the logs, you can access the 
Catalog REST API. Let’s test it out using **curl** in a new terminal window:

`curl http://localhost:9000/api/catalog`{{execute}}

You should see a result like:

```
[{"itemId":"329299","name":"Red Fedora","desc":"Official Red Hat Fedora","price":34.99},...]
```

The REST API returned a JSON object representing the product list. Congratulations!

Stop the service by pressing **CTRL-C** in the terminal window.
