# Charging

Commands related to the charging of the vehicle.

## POST `/api/1/vehicles/{id}/command/charge_port_door_open`

Opens the charge port or unlocks the cable.

### Response

```json
{
  "reason": "",
  "result": true
}
```

## POST `/api/1/vehicles/{id}/command/charge_port_door_close`

For vehicles with a motorized charge port, this closes it.

### Response

```json
{
  "reason": "",
  "result": true
}
```

## POST `/api/1/vehicles/{id}/command/charge_start`

If the car is plugged in but not currently charging, this will start it charging.

### Response

```json
{
  "reason": "",
  "result": true
}
```

## POST `/api/1/vehicles/{id}/command/charge_stop`

If the car is currently charging, this will stop it.

### Response

```json
{
  "reason": "",
  "result": true
}
```

## POST `/api/1/vehicles/{id}/command/charge_standard`

Sets the charge limit to "standard" or ~90%.

### Response

```json
{
  "reason": "",
  "result": true
}
```

## POST `/api/1/vehicles/{id}/command/charge_max_range`

Sets the charge limit to "max range" or 100%.

### Response

```json
{
  "reason": "",
  "result": true
}
```

## POST `/api/1/vehicles/{id}/command/set_charge_limit`

Sets the charge limit to a custom value.

### Parameters

| Parameter | Example | Description                                   |
| :-------- | :------ | :-------------------------------------------- |
| percent   | 75      | The percentage the battery will charge until. |

### Response

```json
{
  "reason": "",
  "result": true
}
```

## POST `/api/1/vehicles/{id}/command/set_scheduled_departure`

Controls all settings for Scheduled departure.

### Parameters

| Parameter                       | Example | Description                                                       |
| :------------------------------ | :------ | :---------------------------------------------------------------- |
| enable                          | true    | Whether to enable Scheduled departure as a whole or not           |
| departure_time                  | 510     | Minutes past midnight in multiples of 15, i.e. `510 = 08:30`      |
| preconditioning_enabled         | true    | Whether to enable climate preconditioning or not                  |
| preconditioning_weekdays_only   | false   | Whether to enable preconditioning for weekdays only or all days   |
| off_peak_charging_enabled       | true    | Whether to enable off-peak charging or not                        |
| end_off_peak_time               | 360     | Minutes past midnight in multiples of 15, i.e. `360 = 06:00`      |
| off_peak_charging_weekdays_only | false   | Whether to enable off-peak charging for weekdays only or all days |



### Response

```json
{
  "reason": "",
  "result": true
}
```

## POST `/api/1/vehicles/{id}/command/set_scheduled_charging`

Controls all settings for Scheduled departure.

### Parameters

| Parameter | Example | Description                                                   |
| :-------- | :------ | :------------------------------------------------------------ |
| enable    | true    | Whether to enable Scheduled charging as a whole or not        |
| time      | 1380    | Minutes past midnight in multiples of 15, i.e. `1380 = 23:00` |



### Response

```json
{
  "reason": "",
  "result": true
}
```
