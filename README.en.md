# Drone Route System – Route Definition Module

This repository provides the files for building a Docker image of the module responsible for defining routes in the Drone Route System.

## Table of Contents

- [System Overview](#system-overview)  
- [Configuration and Setup](#configuration-and-setup)  
- [Build Instructions](#build-instructions)  
- [Startup Instructions](#startup-instructions)  
- [Usage](#usage)  
- [Notes](#notes)  
- [License](#license)  
- [Disclaimer](#disclaimer)  

---

## System Overview

The route definition functionality in the Drone Route System includes the following features:

- Management of maximum drop range  
- Calculation of available space for drone route configuration  
- Management of defined route information  

---

## Configuration and Setup

### Configuration Changes

This module can be configured by modifying the following property files.  
The outline of each property file is as follows:

| File Name                | Location                               | Notes                                                                 |
|---------------------------|----------------------------------------|----------------------------------------------------------------------|
| `application.properties` | `airway-design\src\main\resource`      | Application-specific settings such as thresholds for decision-making |
| `database.properties`    | `airway-design\src\main\resource`      | Database connection details, credentials, and optional parameters used by the container |
| `system.properties`      | `airway-design\src\main\resource`      | Settings for other modules that make up the Drone Route System       |

---

## Build Instructions

To build this module, run the following command:

```bash
./build.sh
````

---

## Startup Instructions

To start this module, run the following command:

```bash
docker compose up -d
```

---

## Usage

### Tips

* Use mock servers for modules that make up the Drone Route System:

  * By using mock servers for counterpart modules, you can verify the operation of the Drone Route System.
  * Applications such as **stoplight/prism**, which can start mock servers from OpenAPI files, can be used.
  * Sample files are provided in the `openAPI` folder.

---

## Notes

* Regarding the term **"Junction"** in the source code:

  * It is used with the same meaning as **"route point"** (a node that separates route sections defined during route determination).

---

## License

* This repository is provided under the **MIT License**.
* Copyright of the source code and related documentation belongs to **IntentExchange Inc.**

---

## Disclaimer

* The contents of this repository may be changed or deleted without prior notice.
* We assume no responsibility for any loss or damage resulting from the use of this repository.
