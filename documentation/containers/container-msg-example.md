---
uid: containerExample
---

# Container Example

### Headers

    omfversion = 1.2
	messagetype = container
	action = create
	messageformat = json

### Body

    [{
		"id": "Tank1_PressureMeasurements",
		"typeid": "TankPressure",
		"datasource":"Modbus",
		"indexes": ["Pressure"],
		"extrapolation": "forward"
	}, {
		"id": "Tank2_PressureMeasurements",
		"typeid": "TankPressure",
		"datasource":"Modbus",
		"indexes": ["Pressure"],
		"extrapolation": "forward",
		"propertyoverrides": {
			"Pressure": {
				"minimum": 15,
				"maximum": 30
			}
		}
	}]
