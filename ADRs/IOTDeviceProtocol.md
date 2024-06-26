# MQTT vs LwM2M vs CoAP
## Status
Accepted

## Context and Problem Statement
We need to select a protocol to send data from IOT devices like water sensors and ojbect recognition cameras to backend systems. There are variety of IOT protocols with their own pros and cons. 

## Requirements
We need to choose a protocol that can support both low bandwidth and high bandwidth situations and is suitable for sending customized data packets.

## Business Assumptions
Sensor devices have either long battery life or have proper power supply available. 

## Decision drivers
We wanted to rely on a protocol that is widely adopted by large number of IOT device vendors. Tomorrow, if we install new devices, it should be easier to make them part of the system. We should be able to track if devices are unreachable or not responding. Devices should be able to upgrade remotely. Protocol should support low bandwidth and high bandwidth situations. Data sent from devices should be consumed by multiple services so that different tasks like monitoring, alerting can be performed by various services. Data needs to be sent to datalake for later retrieval for model optimization and enhancement. 

## Considered options
MQTT/LwM2M/CoAP

## Decision
- Use MQTT for sending data from devices to backend.
- Use LwM2M for device monitoring
