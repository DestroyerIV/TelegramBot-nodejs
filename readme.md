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
   ### Bus  
   * bus.getCalendar(today, datelimit).then...  
   * 
   ```
   bus.getListLines(today, numBus).then...  
```
   ```  
   bus.getListLines(today, datelimit).then(function(res){  
     console.log(res.resultValues)
     })  
```
   * bus.getRouteLines(today, numBus).then...  
   * bus.getTimesLines(today, numBus).then...  
   * bus.getTimeTableLines(today, numBus).then...  
   * bus.getNodesLines(numParada).then...  
   * bus.get.RouteLinesRoute(today, numBus).then...  
   * bus.getGroups().then...  
   
   
