# Starting NGINX
Oh, jeez!
We tried to install NGINX, but it looks like it isn't starting up correctly.

Figure out why, then get it started.

Resist the urge to dig *too* deeply into the Vagrantfile.
Your investigation should be inside the VM.

## Setup
To start the lab, run `vagrant up && vagrant ssh`.

If everything goes sideways, you can restart from scratch with `vagrant destroy -f && vagrant up && vagrant ssh`.

## Victory
Vagrant is forwarding port 80 on the guest machine to port 8080
on your host machine.
Feel free to modify the host port in the Vagrantfile.

On your host machine, visit `localhost:8080` in your browser
or run `curl localhost:8080`.
If you see the default NGINX splash page, you've succeeded!
