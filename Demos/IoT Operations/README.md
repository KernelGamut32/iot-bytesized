# IoT Operations Demo

## AWS IoT Events (https://docs.aws.amazon.com/iotevents/latest/developerguide/what-is-iotevents.html)

Set up a detector model that triggers an action when receiving a high temperature reading (above 80 F):

    - Create one IoT topic called `readings_high_temp`
    - When one the threshold is triggered, publish a message to the appropriate IoT topic
    - Test the receipt of messages on the IoT topic using the high temp readings
    - Alternatively, you can manually post messages in the MQTT test client to create the conditions for triggering the events.