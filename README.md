hl7
=========

HL7 v2 parser/serializer in JavaScript 

Currently supports ORU^R01 (Lab Results) HL7 v 2.3-2.5 messages.

Following segments are implemented:

* MSH - Message Header
* PID - Patient Identification
* OBR - Observation Request
* OBX - Observation Result
* NTE - Notes and Comments

## Example

```
MSH|^~\&|SOME LAB|LAB|HOSPITAL|BLDG4|200202150930||ORU^R01|CNTRL-3456|P|2.4
PID|||555-44-4444||EVERYWOMAN^EVE^E^^^^L|JONES|19620320|F|||153 FERNWOOD DR.^^STATESVILLE^OH^35292||(206)3345232|(206)752-121||||AC555444444||67-A4335^OH^20030520
OBR|1|845439^GHH OE|1045813^GHH LAB|15545^GLUCOSE|||200202150730|||||||||555-55-5555^PRIMARY^PATRICIA P^^^^MD^^|||||||||F||||||444-44-4444^HIPPOCRATES^HOWARD H^^^^MD
OBX|1|SN|1554-5^GLUCOSE^POST 12H CFST:MCNC:PT:SER/PLAS:QN||^182|mg/dl|70_105|H|||F
```


```javascript
[
	["MSH",
	"|",
	"^~\&",
	[["SOME LAB"]]
	...
	],
	["PID",
	[[""]],
	[[""]],
	[["555-444-4444"]],

	]
]
```


##Quick up and running quide

###Prerequisites

- Node.js (v0.10+) and NPM
- Grunt.js

```
# you need Node.js and Grunt.js installed
# and MongoDB + Redis runnning

#install dependencies and build
npm install
grunt

```
## Release Notes

See release notes [here] (./RELEASENOTES.md)

## License

Licensed under [Apache 2.0](./LICENSE)


https://medium.com/vandium-software/5-easy-steps-to-understanding-json-web-tokens-jwt-1164c0adfcec
