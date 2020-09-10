# Priorization in Kafka
Sample code containing a producer and consumer using the [bucket priority pattern implementation](https://github.com/riferrei/bucket-priority-pattern).

## Running

### - Update the configuration

```bash
cd src/main/resources
cp kafka.properties.example kafka.properties
vim kafka.properties
```

### - Building the project

```bash
mvn clean package
```

### - Running the regular producer

```bash
java -cp <CLASSPATH> io.confluent.kafka.demo.AllOrdersProducer
```

### - Running the bucket-based producer

```bash
java -cp <CLASSPATH> io.confluent.kafka.demo.BucketBasedProducer
```

### - Running the regular consumer

```bash
java -cp <CLASSPATH> io.confluent.kafka.demo.AllOrdersConsumer <NUMBER_OF_THREADS>
```

### - Running the bucket-based consumer

```bash
java -cp <CLASSPATH> io.confluent.kafka.demo.BucketBasedConsumer <BUCKET_NAME> <NUMBER_OF_THREADS>
```

# License

This project is licensed under the [Apache 2.0 License](./LICENSE).