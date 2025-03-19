# Pact Broker

## How to view pact contract files

Please make sure to replace `http://localhost` with the actual pact broker url, `ProductPriceService` and `BestPriceFinder` with the actual provider and consumer names.

In the command line, run the following command
```
curl -X GET http://localhost/pacts/provider/ProductPriceService/consumer/BestPriceFinder/latest
```
or 

Use the browser by following the link below

```
http://localhost/pacts/provider/ProductPriceService/consumer/BestPriceFinder/latest
```



## How to run `can-i-deploy` script in command line to check compatibility

Please make sure to replace `http://localhost` with the actual pact broker url, `BestPriceFinder` with the actual consumer name and `0.0.1-SNAPSHOT` with version of the consumer

```
./pact-broker.sh can-i-deploy -a BestPriceFinder -b http://localhost --version 0.0.1-SNAPSHOT
```