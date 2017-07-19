# &Cube-Thyme for Java
## Introduction
&Cube-Thyme is an open source IoT device application entity based on the oneM2M (http://www.oneM2M.org) standard. &Cube-Thyme consists of three versions: Node.js version, Java version and Android version.

## Connectivity stucture
&Cube-Thyme implementation of oneM2M ADN-AE can be connected to MN-CSE or IN-CSE.
<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28315421-497cf0b4-6bf9-11e7-9e67-61e4c351c035.png" width="600"/>
</div>

## Installation
&Cube-Thyme for Java is developed with java.
<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28315422-497d1300-6bf9-11e7-92c7-a0f82d8b4a29.png" width="400"/>
</div><br/>

- [Node.js](https://nodejs.org/en/)<br/>
Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient. Node.js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world. Node.js is very powerful in service impelementation because it provide a rich and free web service API. So, we use it to make RESTful API base on the oneM2M standard.
- [&Cube-Thyme for Node.js](https://github.com/IoTKETI/nCube-Thyme-Nodejs/archive/master.zip)<br/>
&Cube-Thyme for Node.js source codes are written in javascript. So they don't need any compilation or installation before running.

## Configuration
- Open the &Cube-Thyme for Java project
- Modify configuration file "conf.json" per your setting
```
{
    "useprotocol": "http",
    "cse": {
        "cbhost": "203.253.128.161",    //CSE host IP
        "cbport": "7579",               //CSE http hosting port
        "cbname": "Mobius",
        "cbcseid": "/Mobius",
        "mqttport": "1883"              //CSE mqtt broaker port
    },
    "ae": {
        "aeid": "S",
        "appid": "0.2.481.1.1",
        "appname": "ae-test1",          //AE name
        "appport": "9727",
        "bodytype": "xml",
        "tasport": "3105"
    },
    "cnt": [
        {
            "parentpath": "/ae-test1",
            "ctname": "cnt-co2"
        },
        {
            "parentpath": "/ae-test1",
            "ctname": "cnt-led"
        }
    ],
    "sub": [
        {
            "parentpath": "/ae-test1/cnt-led",
            "subname": "sub-ctrl",
            "nu": "mqtt://AUTOSET"
        }
    ]

```
## Export

## Running
Use runnable jar execution command as below
```
java -jar thyme.jar
```

<div align="center">
<img src="https://user-images.githubusercontent.com/29790334/28315420-494a8138-6bf9-11e7-8947-9c0f78b67166.png" width="640"/>
</div><br/>

## Dependency External Libraries
This is the list of external library dependencies for &Cube:Thyme Java 
- org.json
- org.apache.http
- org.eclipse.paho.client.mqttv3

## Document
If you want more details please dowload the full [installation guide document](https://github.com/IoTKETI/nCube-Thyme-Nodejs/blob/master/doc/User_Guide_Thyme_Nodejs_v2.0.0_KR.docx).

# Author
Nak-Myoung Sung (nmsung@keti.re.kr; diesnm201@gmail.com)
