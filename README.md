# nginx
mapping from one port to another

the usage scenario is that there is a coc-server between our server and the public internect.
a tunning is used in coc-server for us to visit our application running on our servers.


in some apache application like hadoop, the url is hard coded like slave1:8042
only editing hosts can't help us beacuse hosts can't mapping port(say 8042 in our example) to another(obviously the tunning port in coc-server is different).


the solution is using nginx in our local machine, and mapping listing to 8042
in hosts mapping slave1 to 127.0.0.1

in this way, all of the request to slave1:8042 will request to our nginx server.
