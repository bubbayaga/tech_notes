
Stream processing, batch-processing framework. 

$employer$ uses [[Kotlin]] with flink.

Flink programs consist of 'streams' and 'transformations'. 

[D] - Stream = 'potentially infinite flow of data records' (e.g. [[Amazon Kinesis]])
[D] - Transformation = 'take one or more streams as input, produce one more output as a result'

Diff APIs for bounded and unbounded data sets. 
Table API ([[SQL]] like language)

All Flink programs map to streaming dataflows - a dataflow starts with one or more sources, ends with one or more sinks. Supports arbitrary number of transformations on stream. 

Offers read -built source + sink connectors for [[Apache Kafka]] and [[Amazon Kinesis]]

Lightweight fault tolerance based on distributed checkpoints ('automatic, async, snapshot of state of app and position in source stream')

Aims for exactly once semantics





can create a Kinesis Data Analytics application by uploading the compiled Flink application jar file to Amazon S3 and specifying some additional configuration options with the service

