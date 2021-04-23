## DDOS

Its a DDOS script written in python.

**DDOS stands for Distributed Denial of Service and it is an attack where we block the ressources of a server by flooding it with requests.**

As target chose an IP of a device you own or have permission to hack (Btw its the default gateway from the ipconfig cmd) and as a fake IP-address I chose a random but still valid address. I decided to attack the port 80, which is HTTP. If you want to shut down a specific service, you need to know which port it is operating at.

The attack function starts an endless loop which creates a socket, connects to the target and sends an HTTP request again and again. And if you are attacking another port, you will also have to change the type of request you send.

Last but not least, we need to do is to run multiple threads that execute this function at the same time.In this case, we are starting 500 threads that will execute our function. Maybe 30 or 50 are already sufficient. 

### Required Modules
- Socket
- Threading
