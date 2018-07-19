# EMT BUS API
**API disponible para servicios de EMT (Empresa Municipal de Transportes)**

![EMT BUS](/img/emt-bus_logo.png)

[![Known Vulnerabilities](https://snyk.io/test/github/lorengamboa/emt-bus/badge.svg)](https://snyk.io/test/github/lorengamboa/emt-bus)

## Requirements
> NodeJS v6+ / [Download NodeJS](https://nodejs.org/es/)  
> OpenData Service Token / Sign up in [Forms](http://opendata.emtmadrid.es/Formulario) and check your mail

## How to Install
This library is installed by npm even though you can also clone the repository  
> `npm install emt-bus --save`

## How to Use
   * Authentication  
   
  > `const EMT = require('emt-bus')`  
   Use this constructor to generate access  
   `EMTToken = new EMT('idClient', 'passKey')`
   
   > Previously we will have to ask for the credentials here
   * Select Category
   * Make a request
