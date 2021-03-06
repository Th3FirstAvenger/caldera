# Pentesting Methodology Framework

The origin of this project is due to the end-of-degree project. My goal is to share my methodology to perform a pentesting attack and others can use it to improve theirs and add content.

Searching I found a very powerful, open source framework for Red and Blue Team.[CALDERA](https://github.com/mitre/caldera), It is built on the MITRE ATT&CK™ framework and is an active research project at MITRE. 

I am not a web developer, so I decided to modify it to get to understand how this framework works and also to take advantage of MITRE Techniques, although the ultimate goal is to obtain a methodology for pentesting attacks. 


## CALDERA INFORMATION

I share the information that CALDERA shows us, but I have eliminated parts that I am not going to use.

1) **The core system**. This is the framework code, consisting of what is available in this repository. Included is 
an asynchronous command-and-control (C2) server with a REST API and a web interface. 
2) **Plugins**. These are separate repositories that hang off of the core framework, providing additional functionality. 
Examples include agents, GUI interfaces, collections of TTPs and more. 

## Plugins

:star: Create your own plugin! Plugin generator: **[Skeleton](https://github.com/mitre/skeleton)** :star:

### Default
- **[Access](https://github.com/mitre/access)** (red team initial access tools and techniques)
- **[Builder](https://github.com/mitre/builder)** (dynamically compile payloads)
- **[Manx](https://github.com/mitre/manx)** (shell functionality and reverse shell payloads)
- **[Sandcat](https://github.com/mitre/sandcat)** (default agent)
- **[Stockpile](https://github.com/mitre/stockpile)** (technique and profile storehouse)

## Requirements

These requirements are for the computer running the core framework:

* Any Linux or MacOS
* Python 3.6.1+ (with Pip3)
* Google Chrome is our only supported browser
* Recommended hardware to run on is 8GB+ RAM and 2+ CPUs

## Installation

- **Docker installation (Recommended)**

```Bash
git clone https://github.com/Th3FirstAvenger/Pentesting-Methodology-Framework.git --recursive --branch tfg
docker-compose up -d
```

- **System installation**

```Bash
git clone https://github.com/Th3FirstAvenger/Pentesting-Methodology-Framework.git --recursive --branch tfg 
cd caldera
pip3 install -r requirements.txt
python3 server.py --insecure
```

Once started, you should log into http://localhost:8888 using the credentials red/admin. Then go into Plugins -> Training and complete the capture-the-flag style training course to learn how to use the framework.

