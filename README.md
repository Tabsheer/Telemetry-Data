# Telemetry Data
### A collection of telemetry captured from SpaceX Launch Webcasts

![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/de/SpaceX-Logo.svg/2000px-SpaceX-Logo.svg.png)


# Structure

The Telemetry is available in three formats: *JSON*, *Excel* and [*JSON Streaming*](https://en.wikipedia.org/wiki/JSON_streaming).

Each directory contain the following files:
* **Launch name raw** - a file contaning the time, velocity and altitude caputred from the webcast in 30 fps.
Usage of this file is not recommended due to the mix of telemetry of the first and second stage (see stage1 raw and stage2 raw below).

* **stage1 raw** - a file contaning the time, velocity and altitude caputred from the webcast in 30 fps of the first stage.

* **stage2 raw** - a file contaning the time, velocity and altitude caputred from the webcast caputred in 30 fps of the second stage.

* **analysed** - a file contaning Telemetry calculated using the raw files.

* **events** - a file contaning the times (rounded to the nearest second) of major events (ex: MECO, Entry Burn Start etc) during the launch.

* **stages** - ???


## Analysed files

These files contain the following fields:

Time (s), Velocity (m/s), Altitude (km), Vertical Velocity (m/s), Horizontal Velocity (m/s), Acceleration (m/s^2) (with gravity), Downrange Distance (km), Velocity Angle (degrees), Aerodynamic Pressure (N).

The files contain data from T+0 until the telemetry is cut. They are only available for a single stage. The analysed stage can be found in the [Launches](https://github.com/shahar603/Telemetry-Data/raw/master/Laucnhes.json) file in the field ```analysed_stage```


The [Launches](https://github.com/shahar603/Telemetry-Data/raw/master/Laucnhes.json) JSON file contains links to each file of each launch.

The flight_number is consistant with the [r-spacex database](https://github.com/r-spacex/SpaceX-API)

## Example

This is the JSON Object representing the Orbcomm OG2 launch.

```
{
        "mission_name": "Orbcomm OG2",
        "flight_number": 25,
        "analysed_stage": 2,
        "Excel": {
            "raw": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/Excel/Orbcomm%20OG2%20raw.xlsx",
            "stage1": null,
            "stage2": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/Excel/stage2%20raw.xlsx",
            "analysed": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/Excel/analysed.xlsx",
            "events": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/Excel/events.xlsx"
        },
        "JSON": {
            "raw": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON/Orbcomm%20OG2%20raw.json",
            "stage1": null,
            "stage2": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON/stage2%20raw.json",
            "analysed": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON/analysed.json",
            "events": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON/events.json",
            "stages": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON/stages.json"
        },
        "JSON STREAMING": {
            "raw": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON%20STREAMING/Orbcomm%20OG2%20raw.json",
            "stage1": null,
            "stage2": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON%20STREAMING/stage2%20raw.json",
            "analysed": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON%20STREAMING/analysed.json",
            "events": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON%20STREAMING/events.json",
            "stages": "https://raw.githubusercontent.com/shahar603/Telemetry-Data/master/Orbcomm%20OG2/JSON%20STREAMING/stages.json"
        }
}
```

* I am not affiliated with SpaceX in any way, shape, form.
* All the Telemetry was captured from SpaceX' webcasts
