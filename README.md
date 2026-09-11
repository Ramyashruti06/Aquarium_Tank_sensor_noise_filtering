# Aquarium_Tank_sensor_noise_filtering

# OBJECTIVE 
To simulate the readings from 3 sensors – Turbidity sensor, DHT22 (Temperature and Humidity) sensor, Water level sensor using MATLAB, accompanied by realistic noise and applying a moving filter and comparing it against a Kalman filter for accurate readings.

# METHODOLOGY 
Sensor readings are combined with noise to mimic real-time sensor readings. Filters - Kalman filter & Moving Average are used to generate actual readings of those signals.

# PARAMETERS 
1.	t => Time in min for 1 day
2.	windowSize = 15 => moving average window
3.	Q = 0.01 => Process noise estimate [Kalman filter tuning]
4.	R = 0.25 => measurement noise estimate [Kalman filter tuning]
5.	DHT22 Temperature noise signal = ±0.5°C 
6.	DHT22 Humidity noise signal = ±2%
7.	Turbidity noise signal = ±2% NTU
8.	Water level noise signal = ±0.3 cm
9.	rng(42) => a random integer set to 42

# CODE 
The source code is available at [https://github.com/Ramyashruti06/Aquarium_Tank_sensor_noise_filtering/blob/main/Tank_sensor_code]

# GRAPHS 
Temperature Filtering - 
<img width="1119" height="674" alt="temperature_filtering" src="https://github.com/user-attachments/assets/f06d91e5-0a58-4b7a-a379-65c67a796d6f" />

Humidity Filtering -
<img width="1119" height="674" alt="humidity_filtering" src="https://github.com/user-attachments/assets/7a5d81a3-d3f6-4864-bee3-ee0c5ce7c248" />

Turbidity Filtering - 
<img width="1119" height="674" alt="turbidity_filtering" src="https://github.com/user-attachments/assets/0b2cd2cb-68e8-43b5-9817-416ce532b09c" />

Water-level Filtering - 
<img width="1119" height="674" alt="water_level_filtering" src="https://github.com/user-attachments/assets/4c87c584-0b19-40f9-b914-e841deef1d3b" />

# RESULTS 
RMSE of each sensor - 

| Sensor | Kalman filter RMSE | Moving Average RMSE |
|:---|:---:|---:|
| DHT22 Temperature | 0.276 | 0.244 |
| DHT22 Humidity | 0.639 | 0.500 |
| Turbidity | 0.744 | 0.504 |
| Water-level | 0.092 | 0.074 |

# OBSERVATIONS 
- When a noise signal is added to the sensor to replicate real-time sensor readings and these are filtered using Kalman filter and Moving Average techniques, a graph depicting all 4 signals for each sensor module is shown.
- This graph does not differentiate which filter gives accurate readings compared to other filter. Both filter signals seem to align each other closely.
- In order to determine which filter works better, RMSE method is implemented.
- This method calculates the difference (Filtered signal - true signal) and gives a number in decimals.
- From the above RMSE table, it can be observed that Moving Average gives precise readings compared to Kalman filter.
- This is because for Kalman filter, noise tuning parameter (Q = 0.01) was tuned very low, causing filter to depend on its estimate rather than incoming sensor readings.

# LIMITATIONS 
Though this project imitates real-time sensor readings, it is based on datasheet estimates. This can impact the readings.

# FUTURE SCOPE 
With the calibration of sensor readings, noise signal and filters, a sensed signal is obtained. In the future, this can be coordinated with hardware setup for full-scale automation. 

# PROJECT STATUS 
MATLAB simulated project.

# AUTHOR 
KOTIKALAPUDI RAMYA SHRUTI
