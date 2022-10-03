# Client-Server-Trading-System
About Developed a client-server-based trading system facilitating ṭraders for buying and selling of varying quantities of items listed.The client can perform functionalities such as login to the system, sending buy or sell request, view order status, view trade status.

Steps to run the code

1.Use linux and make sure that all the systems that are being used are connected to a single network.

2.Run Server on one system with command ./server ⟨server port⟩.

3.Run Clients on other systems with command ./client ⟨server ip⟩ ⟨server port⟩.

4.Client can type the following commands (a) register Using this command a new trader can register to the trading application. (b) login Using this command an existing trader can login to the application. (c) buy This command is used to place a buy order. (d) sell This command is used to place a new sell order. (e) order This command shows the current best buy price and sell price for each item. (f) trade This command shows the matched orders for a trader. (g) logout This command is used to logout from the application. (h) close This command is used to close the client. Any other command will print What are you saying?

5.Follow the instructions printed on terminal properly to avoid errors during execution.


Assignment Group 17 (Application 2 - Trading System) - by

--> Senapathi Akhila preethi(214101050)
--> Shambhavi Shanker(214101051)
--> Sherin Abraham(214101052)



This application contains following files
--------------------------------------------------------
--> server.c - C code file for server
--> server.h - header file for server 
--> client.c - C code file for client
--> credentials.txt - contains login credentials (trader id, user name, password)
--> makefile - for compiling client and server code.


Compiling files
--------------------------------------------------------
For Server ::::::::
make server

For Client ::::::::
make client

Executing 
--------------------------------------------------------
For Server ::::::::
./server <SERVER PORT NUMBER>

For Client ::::::::
./client <Server IP Address> <SERVER PORT NUMBER>

---->use a port number greater than or equal to 1024

********************************************************

Client Queries
     -> Typed username and passwords are first verified using the credential.txt file
     -> After verification Trader ID is also asked 
     (First column in credential.txt is the Trader ID, second column is user name and third column is password)
     -> Asked responses are seperated by white spaces 

Request Types -------------------------------------

     -> Login request
          <Log-IN ID> <PASSWORD> L $

     -> Buy request
          <Log-IN ID> <PASSWORD> B <item-code> <qty> <unit-price> $

     -> Sell request
          <Log-IN ID> <PASSWORD> S <item-code> <qty> <unit-price> $

     -> View Trades
          <Log-IN ID> <PASSWORD> VT $

     -> View orders
           <Log-IN ID> <PASSWORD> VO $


Server Responses -------------------------------------------------------------------------------------------------------------------

- Common response format
    Any of the mentioned points in Request Types accordingly 

- Response for sign in request:
    ACCEPTED -
>>>Login Successfull for Trade ID: 3
