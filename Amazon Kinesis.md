

Collect, process, and analyze real-time video and data streams (presumably relating to [[reactive programming]])

Subtypes:

* Data Streams - serverless streaming data service that simplifies the capture, processing, and storage of data streams at any scale.
* Firehose - extract, transform, and load (ETL) service that reliably captures, transforms, and delivers streaming data to data lakes, data stores, and analytics services.
* Data Analytics - uses [[Apache Flink]] to transform and analyze streaming data 
* Video Streams ($employer$ must be using this??) - "more easily and securely stream video from connected devices to AWS for analytics, ML, playback, and other processing." // very vague

## Kinesis Video Streams

Auto provision and scale
Stores on S3
Live + On Demand via Kineses Video Streams HTTP Live Stream (HLS) capacity
Integrate with [[Amazon Rekognition Video]], ML frameworks 
Uses WebRTC , 2 way real time media streaming
Secure via [[AWS Key Management Service (KMS)]] and [[TLS]] 
"Infraless"

Sources:

https://aws.amazon.com/kinesis/
https://aws.amazon.com/blogs/big-data/streaming-etl-with-apache-flink-and-amazon-kinesis-data-analytics/