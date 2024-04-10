# Parking-occupancy-node-with-ESP32
Project held at the Politecnico di Milano in the exam "Internet of Things" held by Prof. Cesena, Prof Boiano and Prof. Palmese.

The aim of this project is to develop and simulate on WokWi a simple parking occupancy node using an ESP32 microcontroller and the HC-SR04 ultrasonic distance sensor. 

The parking node communicate to a central ESP32 sink node the occupancy of a parking slot using the HC-SR04 ultrasonic distance sensor to estimate the presence of a car in a parking spot (distance < 50 cm). In order to save energy, the sensor node implements a duty cycle, where every 14 seconds it wakes up from Deep sleep and transmit a String «FREE»/«OCCUPIED» to the ESP32 sink node, to state if the parking spot is empty/occupied by a car. As soon as the transmission is performed, the node goes back in Deep Sleep state. The sensor node will communicate the presence of a car using the ESPNOW protocol to a central ESP32 sink node (The sink node has no energy constraints).

In the end, some considerations regarding energy consuption and battery lifetime are made.
