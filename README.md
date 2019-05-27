# KafkaToVertica


Source: MySQL
Target: Vertica
Messaging Layer: Kafka

Pre-Requestes:
1. This programs processes the events produced by Maxwell daemon.
http://maxwells-daemon.io/
2. Kafka and Zookeper is already setup and Maxwell daemon is sending the CDC events to kakfa. 
3. Vertica is setup. 
4. You have CDC table created in vertica mataching source table. 


This program currently caonverts json payload produced by Maxwell and filters the inserts events and insert it to vertica table.

1. Reading from kafka.
2. Transform json object to required field.
3. Filtering the Insert events corrosponds to target table.
3. Converting cdc this operations in insert statements to write to vertica.

