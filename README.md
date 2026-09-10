# Aquarium_Tank_sensor_noise_filtering

# OBJECTIVE - 
To simulate the readings from 3 sensors – Turbidity sensor, DHT22 (Temperature and Humidity) sensor, Water level sensor using MATLAB, accompanied by realistic noise and applying a moving filter and comparing it against a Kalman filter for accurate readings.

# METHODOLOGY - 
Sensor readings are calibrated with noise to mimic real-time sensor readings. Filters - kalman filter & Moving Average are used to generate actual readings of those signals.

# PARAMETERS - 
1.	t => Time in min for 1 day
2.	windowSize = 15 => moving average window
3.	Q = 0.01 => Process noise estimate [Kalman filter tuning]
4.	R = 0.25 => measurement noise estimate [Kalman filter tuning]
5.	DHT22 Temperature noise signal = ±0.5°C 
6.	DHT22 Humidity noise signal = ±2%
7.	Turbidity noise signal = ±2%
8.	Water level noise signal = ±0.3 cm
9.	rng(42) => a random integer set to 42

# CODE - 

