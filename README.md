# ft_irc - Internet Relay Chat Server

## Description
ft_irc is an implementation of an Internet Relay Chat (IRC) server, developed as part of the 42 school common core. This project involves creating a server that can handle multiple clients, manage channels, and process IRC commands according to the IRC protocol specifications.

## Features
- Multi-client support with non-blocking I/O
- Channel management (create, join, kick, etc.)
- Basic IRC commands implementation
- User authentication and registration
- Message broadcasting and private messaging
- Channel modes and operators
- Error handling and logging

## Project Structure
```
ft_irc/
├── include/         # Header files
├── src/            # Source files
│   ├── commands/   # IRC command implementations
│   ├── Channel.cpp # Channel management
│   ├── Client.cpp  # Client handling
│   ├── Server.cpp  # Server core functionality
│   ├── parsing.cpp # Message parsing
│   └── main.cpp    # Program entry point
└── Makefile        # Build configuration
```

## Requirements
- C++ compiler (C++98 standard)
- Make
- Unix-like operating system

## Building
To build the project, simply run:
```bash
make
```

## Usage
To start the server:
```bash
./ircserv <port> <password>
```
- `<port>`: The port number on which the server will listen
- `<password>`: The server password required for client connection

## IRC Commands
The server supports the following IRC commands:
- PASS: Login to the server
- NICK: Change nickname
- USER: Set username and realname
- JOIN: Join a channel
- PRIVMSG: Send private message
- KICK: Remove user from channel
- INVITE: Invite user to channel
- TOPIC: Set channel topic
- MODE: Set channel modes

## Technical Details
- Uses non-blocking I/O with poll() for efficient client handling
- Implements the IRC protocol as specified in RFC 1459
- Handles multiple clients simultaneously
- Supports channel modes and operators
- Implements proper error handling and logging

## Error Handling
The server implements comprehensive error handling for:
- Invalid commands
- Connection issues
- Channel operations
- User authentication
- Message formatting 