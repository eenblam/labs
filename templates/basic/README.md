# Basic template
This Vagrantfile provides a client with no internet access
but with access to the server.
Maybe you want the client to route through the server,
or maybe you just don't want the client to reach the Internet at all.

The client could always reach the internet by running
`sudo ip r r default via 10.0.2.2 dev eth0`,
but this defeats the purpose of the exercise.
