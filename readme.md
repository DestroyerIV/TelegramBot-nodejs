# EMT BUS API Library  

![EMT BUS](/img/emt-bus_logo.png)

[![Known Vulnerabilities](https://snyk.io/test/github/lorengamboa/emt-bus/badge.svg)](https://snyk.io/test/github/lorengamboa/emt-bus)

## Requirements
> NodeJS v6+ | [Download NodeJS](https://nodejs.org/es/)  
> OpenData Service Token | Sign up in [Forms](http://opendata.emtmadrid.es/Formulario) and check your mail

## How to Install
This library is installed by npm even though you can also clone the repository  
> `npm install emt-bus --save`

## How to Use
   ### Authentication  
  > *Call the library*  
  `const EMT = require('emt-bus')`  
   
  >*Use this constructor to generate access to the service*  
   `EMTToken = new EMT('idClient', 'passKey')`
   
   > Previously we will have to ask for the credentials [here](https://github.com/DestroyerIV/TelegramBot-nodejs/blob/master/readme.md#requirements)
   ### Select Category  
  > *Establish the service to request*  
   `var bus = EMTToken("bus")` or `var geo = EMTToken("geo")`
   ### Make a request  
  > *we will make a basic request in the following way*  
  `bus.getCalendar(today).then(function(res){  
  })`
   
