
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/DeMaCS-UNICAL/EmbASPServerExecutor/master/LICENSE)
[![GitHub release](https://img.shields.io/github/release/DeMaCS-UNICAL/EmbASPServerExecutor.svg)](https://github.com/DeMaCS-UNICAL/EmbASPServerExecutor/releases/latest)
[![GitHub issues](https://img.shields.io/github/issues/DeMaCS-UNICAL/EmbASPServerExecutor.svg)](https://github.com/DeMaCS-UNICAL/EmbASPServerExecutor/issues)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/DeMaCS-UNICAL/EmbASPServerExecutor.svg?style=social)](https://twitter.com/intent/tweet?text=Wow:&url=%5Bobject%20Object%5D)

# EmbASPServerExecutor
_EmbASPServerExecutor_ is a Java application that is able to execute ASP programs with different solvers, using the [EmbASP](https://github.com/DeMaCS-UNICAL/EmbASP) framework.
It runs on top of _Apache Tomcat&reg;_ and it exposes a set of API that can be used to invoke the solvers.
It uses _WebSocket_ as communication protocol and _JSON_ ad data interchange format.


## IMPORTANT NOTE

__*EmbASPServerExecutor started as an undergraduate student's work of thesis, and is still at the early stages of development.*__

__*It currently supports only two solvers (DLV and Clingo) for Answer Set Programming; we encourage any feedback, but we do NOT recommend it for production yet.*__


## Getting Started (Installation and Usage)
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
It requires only [Java&reg;](http://oracle.com/java) and [Apache Tomcat&reg;](http://tomcat.apache.org)

### Installing
Download the [Latest Release](../../releases/latest) of _EmbASPServerExecutor_

Deploy `EmbASPServerExecutor.war` in Tomcat:
 1. Go to Tomcat webapps folder and paste it.
 1. Go to `Tomcat/bin` folder and start Tomcat by clicking *startup.bat* for Windows, for Linux run *startup.sh*
 1. Go to `webapps/EmbASPServerExecutor/WEB-INF/classes/resources` folder and change the value **absolute_path** in *config.properties* file with your absolute path of the ASP solvers (substitute `$CATALINA_BASE` with the path of your Tomcat installation, it is shown when you start Tomcat)
 1. Restart Tomcat (or just restart the _EmbASPServerExecutor_ application)

Note that on Linux systems you may need to change the _Execute_ permission of the files in the [WebContent/WEB-INF/lib](https://github.com/DeMaCS-UNICAL/EmbASPServerExecutor/tree/master/WebContent/WEB-INF/lib) folder.

### Running
Can be invoked using the WebSocket protocol, as explained in the [Wiki](https://github.com/DeMaCS-UNICAL/EmbASPServerExecutor/wiki/APIs)

## Built With
 - [EmbASP](https://www.mat.unical.it/calimeri/projects/embasp) - To execute logic programs with different solvers
 - [Gson](https://github.com/google/gson) - To convert Java Objects into JSON and back
 - [timeout](http://coldattic.info/page/resourcelimit) - To limit time and memory consumption of the executors under Linux

<!-- 
## Contributing

Please read [CONTRIBUTING.md]() for details on our code of conduct, and the process for submitting pull requests to us.
 -->

## Versioning
We use [Semantic Versioning](http://semver.org) for versioning. For the versions available, see the [releases on this repository](https://github.com/DeMaCS-UNICAL/EmbASPServerExecutor/releases). 


## Credits
 - Eliana Palermiti
 - Stefano Germano
 - Francesco Calimeri

From the [Department of Mathematics and Computer Science](https://www.mat.unical.it) of the [University of Calabria](http://unical.it)


## License
  This project is licensed under the [MIT License](LICENSE)
