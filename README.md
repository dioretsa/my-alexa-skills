# my-alexa-skills
This repository contains my Alexa custom skills. I use some of these skills to monitor and control my home automation system with voice. Skills connect to my home automation system by using RESTful API calls. Home automation skills have currently not been published 'alive' since the REST API they use is completely customized for my own home. Some of the skills are coded just for fun, quickly and buggy. You have been warned :) 

## lights-control
This skill provides capability to switch on/off lights at my home. Lights are driven by IHC which is connected to home automation via RS-232 link. For example: Alexa, ask lighs control to switch on kitchen. 

## heating-control
This skill is capable of monitoring and controlling Mitsubishi FD35 air-to-air heat pump. The pump is diven by a custom made IR remote which is connected to home automation. For example: Alexa, ask heating control to set temperature 23.

## home-measurements
This skill is capable of monitoring some temperature and electric power consumption parameters. Temperature measurements are based on 1-wire sensors and power consumption on Cost Control receiver/display and a buch of transmitter modules. For example: Alexa, ask my home power consumption.

## time-table
This skill can query [Reittiopas API](http://developer.reittiopas.fi/pages/fi/http-get-interface-version-2.php?lang=EN) public transport time tables and speaks departure times for your preferred bus and train stops. For example: Alexa, ask time tables next train.
The AWS Lambda function expects the following environment variables:
- user: reittiopas API user name
- passwd: reittiopas API password
- train_stop: your local train stop code e.g. E5142
- bus_stop: your local bus stop code e.g. E5238
- lines: your preferred bus/train lines in comma separated list e.g. 2065  1,2065K 1,3002E 2,3002L 2,3002L62,3002U 2,3002U32
- application_id: your alexa skill's application id

## euribor (live)
This skill reads latest Euribor interest rates and speaks them. This skill is currently alive and can be invoked with name 'Rates Tracker'. For exmaple: Alexa, ask Rates Tracker to get rates. 

## my-weather (live)
This skill reads weather observations and forecasts for a given place in Finland from FMI open data . See more documentation [here](https://alexapublic.s3.amazonaws.com/my-weather.html). 

## air-quality
This skill reads air quality observations and forecasts for a given place in Finland from FMI open data. See more documentation [here](https://alexapublic.s3.amazonaws.com/air-quality.html). 

## my-earth (live)
This skill reads CO2 weekly amounts (now, 1 year ago and 10 years ago) measured by NOAA. For example: Alexa, ask my earth CO2.

## finn-kino
This skill reads movies currently playing at Finnkino theatres in Espoo Iso-omena. 

## TODO
- Integrate my Vaisala GMW90 wall transmitter to home automation system and make Alexe speak measured parameters.
