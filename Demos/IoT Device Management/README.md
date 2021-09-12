# IoT Device Management Demo

## AWS IoT Core (https://docs.aws.amazon.com/iot/latest/developerguide/what-is-aws-iot.html)

- Create 3 EC2 instances to represent 3 different temperature & humidity sensors
- Configure in IoT Core
- For "device" 1:
    - Payload: `{
    "device_name": "THSensor01",
    "readings": {
        "temperature": 72,
        "humidity": 0.55
    },
    "timestamp": "<date/time value>"
    }`
    - Will continue to send readings (temperature in Fahrenheit, humidity as a %) every 5 seconds until stopped
    - Will send a high temperature value of 89 Fahrenheit for every 10th reading
- For "device" 2:
    - Payload: `{
    "device_name": "THSensor02",
    "measurements": {
        "temp": 19.4,
        "hum": 0.55
    },
    "timestamp": "<date/time value>"
    }`
    - Will continue to send readings (temperature in Celsius, humidity as a %) every 10 seconds until stopped
    - Will send a high temperature value of 31.1 Celsius for every 15th reading
- For "device" 3:
    - Payload: `{
    "device_name": "THSensor03",
    "tempdata": 68,
    "timestamp": "<date/time value>"
    }`
    - Will continue to send readings (temperature in Fahrenheit, humidity as a %) every 7 seconds until stopped
- Walk attendees through configuration
- Log on to each "device" and talk about the NodeJS code used to post readings for each device type
- Post all readings to a topic called "readings" and demo data coming through according to requirements
