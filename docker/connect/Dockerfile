FROM confluentinc/cp-server-connect-base:7.9.0

RUN   confluent-hub install --no-prompt debezium/debezium-connector-mysql:3.0.8 && \
      confluent-hub install --no-prompt debezium/debezium-connector-mongodb:3.0.8 && \
      confluent-hub install --no-prompt mongodb/kafka-connect-mongodb:1.16.0

COPY rds-truststore.jks /home/appuser/rds-truststore.jks
COPY debezium-jdbc-sink /usr/share/confluent-hub-components/debezium-jdbc-sink
