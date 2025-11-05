# 🗣️ Minitalk

> A small data exchange program using UNIX signals — part of the 42 curriculum.  
> The goal is to code a client and server that communicate via **SIGUSR1** and **SIGUSR2** signals.

## 🚀 Overview
**Minitalk** is a simple communication program between a server and a client using only UNIX signals (`SIGUSR1` and `SIGUSR2`).  
The **server** receives messages from the **client**, which sends them **bit by bit** using these two signals.

## ⚙️ How It Works
1. The server starts first and prints its **Process ID (PID)**.  
2. The client takes the server’s PID and a string as arguments.  
3. The client converts each character into binary and sends it:
   - `SIGUSR1` → bit `0`
   - `SIGUSR2` → bit `1`
4. The server reconstructs the message bit by bit and displays it when complete.
