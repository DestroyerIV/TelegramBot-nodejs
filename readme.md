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
   > We leave these two variables specified. 'today' would be responsible for obtaining the current day and 'numBus' would be the number of the bus to consult
   ### Bus   
   > Get information about whether there is a day that is a holiday - Saturday - Labor with the display of specific dates.
   ```js
   bus.getCalendar(today, datelimit).then(function(res){  
     console.log(res.resultValues)
     });
```  
   > Retrieves general information about the bus lines and subgroup to which it belongs..
   ```js  
   bus.getListLines(today, numBus).then(function(res){  
     console.log(res.resultValues);
     });  
```  
   > Get the itinerary of a line or variable separated by ( | ). It also obtains the coordinates and name of the stops.
.
   ```js
    bus.getRouteLines(today, numBus).then(function(res){  
      console.log(res.resultValues);
      });  
```     
   > Get the itinerary of the arrival frequency schedules to the stop, or when the service starts and ends.
Bus schedules depending on whether it is working, Saturday or holiday.    
   ```js
   bus.getTimesLines(today, numBus).then(function(res){  
     console.log(res)
     });  
```     
   > Get the frequency time a bus passes.
   ```js
   bus.getTimeTableLines(today, numBus).then(function(res){  
     console.log(res);
     });  
```  
   > Retrieve all stop identifiers with their respective coordinates, their name and the relation between line and direction of them.

   ```js
   bus.getNodesLines(numParada).then(function(res){  
     console.log(res)
     });  
```  
   > All the lines through which each bus passes.

   ```js
   bus.get.RouteLinesRoute(today, numBus).then(function(res){  
      console.log(res)  
     });  
```  
   > Returns the data of the different types of networks of the EMT lines.

   ```js
   bus.getGroups().then(function(res){  
     console.log(res)
     });  
```
   
