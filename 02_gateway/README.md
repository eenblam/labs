# 02: Gateway
You found a neat server sitting out on the curb,
and you were able to get Debian on it. Cool!
You want to use it as a gateway for your Debian PC,
but it doesn't seem to be forwarding traffic.
What gives?

Platform: currently works only on Linux hosts.

## Setup
Open two terminals.
Run `vagrant up` to start the lab.
Once complete, run `vagrant ssh pc` in one terminal
and `vagrant ssh gateway` in the other.

## Task
Update the gateway's network configuration until the "PC"
can successfully reach GitHub.
(e.g. you receive response packets from `ping github.com`)

Don't make any changes to the network configuration of the client.
Running `sudo ip route replace default via 10.0.2.2 dev eth0`
will get you Internet access through Virtualbox,
but that interface only exists to allow you to SSH into the machine.

## Troubleshooting
If `vagrant up` doesn't work,
post an issue to https://github.com/eenblam/labs/issues.

If you've lost track of your changes to the gateway,
or if you've broken networking and lost access to the gateway,
you can restart from scratch by running
`vagrant destroy -f && vagrant up`.
