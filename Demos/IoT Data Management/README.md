# IoT Data Management Demo

## AWS IoT Analytics (https://docs.aws.amazon.com/iotanalytics/latest/userguide/welcome.html)

Set up a channel, data store, pipeline, and data set for aggregating and processing temperature and humidity readings from the three (3) devices using the defined topic of "readings". Implement the following pipeline activities for "intelligent" processing of the incoming data:

    - Use a Lambda transform activity to normalize data format for incoming telemetry to a common format of `{ "device_name": "<device name>", "temperature": <temperature value>, "humidity": <humidity value (if present)>, "timestamp": "<date/time value>" }`
    - Use the same transform operation to convert temperature on all incoming telemetry readings to Fahrenheit
    - In the Lambda function, route the transformed & filtered data into an S3 bucket for data storage (using `<group name>` in the topic name for distinction from other implementations)
