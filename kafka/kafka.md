# Kafka

## Setup

### Run kafka

go run main.go -brokers="`oc get routes my-cluster-kafka-bootstrap -o=jsonpath='{.status.ingress[0].host}{"\n"}'`:443" -verbose=true -ca=ca.crt -verify=false

### Verify kafka

./kafka-console-consumer.sh --bootstrap-server my-cluster-kafka-bootstrap-kafka.apps.ocp67.ajco.se:443 --from-beginning --topic my-topic --consumer.config client.properties

```shell
cat client.properties
security.protocol=SSL
ssl.truststore.location=kafka.server.truststore.jks
ssl.truststore.password=XXX
```
