# Drone route system Route classification module

This repository publishes a file that creates a module that defines the route in the drone route system as a Docker image.

## Table of Contents

- [System Overview] (# System Overview)
- [Building and Setting] (# Construction and Setting)
- [Build method] (#build method)
- [Start-up method] (#start-up method)
- [How to use] (# How to use)
- [Notes] (# Precautions)
- [License] (#License)
- [Disclaimer] (#Disclaimer)

## System Overview

The route classification has the following functions in the drone route system.
- Maximum drop range management
- Calculation of the space where the drone route can be set
- Management of defined route information

## Construction and Setup

### Change of settings

This module can be changed by modifying the following property file.  
The overview of each property file is as follows.

|File name|Placement location|Remarks|
|-|-|-|
|application.propeties|airway-design\src\main\resource| Include application-specific settings and judgment thresholds|
|database.properties|airway-design\src\main\resource| Include the connection destination, credentials, and optional parameters of the DB used by the container|
|system.properties|airway-design\src\main\resource|Settings for other modules that make up the drone route system|

## How to build

To build this module, execute the following command.

"The Bash"
bash ./build.sh
`` `

## How to start

To start this module, execute the following command.

"The Bash"
docker compose up - d
`` `

## How to use

### Tips

- Using the mock server of the module that makes up the drone route system
  - By using the oncoming module as a mock server, you can check the operation of the drone route system.
  - [stoplight/prism] (https://docs.stoplight.io/docs/prism/f51bcc80a02db-installation#docker) and other applications that launch mock servers using openAPI files are used.
  - A sample of the file is placed in the openAPI folder.

## Precautions

- About the notation "Junction" in the source code
  - It is used in the same sense as "route point" (separating the route compartment set at the time of the route is decided).

## License

- This repository is provided under the MIT license.
- The copyright of the source code and related documents belongs to IntentExchange Co., Ltd.

## Disclaimer
- The contents of this repository are subject to change or deletion without notice.
- We shall not be liable for any loss or damage caused by the use of this repository.
