# EMT BUS API Library  

![EMT BUS](/img/emt-bus_logo.png)

[![Known Vulnerabilities](https://snyk.io/test/github/lorengamboa/emt-bus/badge.svg)](https://snyk.io/test/github/lorengamboa/emt-bus)  
# Information  
* [Requirements](https://github.com/DestroyerIV/TelegramBot-nodejs/blob/master/readme.md#requirements)
* [How to install](https://github.com/DestroyerIV/TelegramBot-nodejs/blob/master/readme.md#how-to-install)  
* [How to Use](https://github.com/DestroyerIV/TelegramBot-nodejs/blob/master/readme.md#how-to-use)  
* [Methods]()  


## Requirements
> NodeJS v6+ | [Download NodeJS](https://nodejs.org/es/)  
> OpenData Service Token | Sign up in [Forms](http://opendata.emtmadrid.es/Formulario) and check your mail

## How to Install
This library is installed by npm even though you can also clone the repository.
>   
```  
npm install emt-bus --save  
```

## How to Use
   ### Authentication  
  > *Call the library and use constructor to generate access to the service*  
  ```js
  const EMT = require('emt-bus')
  EMTToken = new EMT('idClient', 'passKey')
```  

   > Previously we will have to ask for the credentials [here](https://github.com/DestroyerIV/TelegramBot-nodejs/blob/master/readme.md#requirements)
   ### Select Category  
  > *Establish the service to request*  
   ```js
   var bus = EMTToken("bus")
   ```  
   or  
   ```js
   var geo = EMTToken("geo")  
   ```  
   
   ### Make a request  
  > *We will make a basic request in the following way. the property 'today' it's the current day and datelimit is the deadline*  
   ```js
bus.getCalendar(today, datelimit).then(function(res){  
console.log(res.resultValues);  
})  
   .catch(function(error){  
console.log(error)  
});
```
   ## Methods
   ### 🚌 Bus Methods 

|   Methods| Description | Parameters |
| ---------|-------------|------------|
| getCalendar|Get EMT Calendar for all days and line schedules for a range of dates   
| getGroups|Returns every line type and their details |
| getListLines|Returns lines with description and groups     |
| getNodesLines|Returns all stop identifiers and his coordinate, name, lines and directions|
| getRouteLines| Returns a line/s route with the vertex info to build the route and coordinates for stops and axes |
| getTimeTableLines|Provices information about the requested line at travel time|
| getTimesLines|Returns current schedules for the requested lines|

### 🌍 Geo Methods 

|   Methods|Description |
| ---------|-------------|
| getArriveStop|Gets bus arrive info to a target stop |
| getGroups|Return a list of groups |
| getInfoLine|Returns line info in a target date|
| getInfoLineExtend|Returns line info in a target date|
| getPointsOfInterest|Returns a list of Points of Interest from a coordinate center with a target radius|
| getPointsOfInterestTypes|Returns a list of Point of interest types|
| getStopsFromStop|Returns a list of stops from a target stop with a target radius and the lines arriving to those stops.|
| getStopsFromXY|Returns a list of stops from a coordinate with a radius and the lines arriving to those stops.|
| getStopsLine|Provices information about the requested line at travel time.|
| getStreet|Returns a list of EMT nodes related to a location. All EMT locations are a group of stops  within a target radius and the lines related to each stop in the list.|
| getStreetFromXY|Returns a list of stops from a target coordinate.|

### 📺 Media Methods(WIP)

|   Methods|Description |
| ---------|-------------|
| getEstimatesIncident| Get estimate arrival time to stop and its related issues
| getStreetRoute|Request up to three optimal routes from one place to another using bus or walking, source and destination must be in a format known for the system, which means that should have been validated by a GetStreet call   
| getRouteWithAlarm| |
| getRouteWithAlarmResponse| |
| getRoute| |
| getRouteResponse| |

### 🚲 Bike Methods 

|   Methods|Description |
| ---------|-------------|
| getStations|Obtiene la relación de todas las bases de Bicimad y su estado operacional. |
| getSingleStations|Obtiene la información de una base |

### 🅿 Parking Methods (WIP)

|   Methods|Description |
| ---------|-------------|
| detailParking|N/A |
| detailPOI|N/A |
| iconDescription|N/A|
| infoParkingPoi|N/A|
| listFeatures|N/A|
| listParking|N/A|
| listStreetPoisParking|N/A|
| listTypesPOIs|N/A|
