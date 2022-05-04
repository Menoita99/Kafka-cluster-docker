# Kafka-cluster-docker

Starts a simple kafka cluster with 1 instance of zookeper, 3 kafka brookers and
the intuitive ui "UI for Apache Kafka" https://github.com/provectus/kafka-ui.

# To Test a cluster:


You should test using the ui that is available at port 7070 (http://localhost:7070)

If you want to test inside a kafka brooker container use:

https://docs.bitnami.com/google-templates/infrastructure/kafka/administration/create-cluster/#testing-the-cluster

Change directory:
```
cd /opt/bitnami/kafka/bin
```
Producer
```
kafka-console-producer.sh --broker-list kafka1:9092 --topic test
```
Consumer
```
kafka-console-consumer.sh --bootstrap-server kafka2:9092 --topic test --from-beginning
```