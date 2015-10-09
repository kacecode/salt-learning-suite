#Salt Learning Suite#

This project uses docker-compose to allow you to easily emulate master/minion environments for learning salt.

## Install ##
Relies on docker and docker-compose.

See (Docker)[https://docs.docker.com/installation/] for install notes.

Docker-compose is installed via pip.


## Usage ##
`docker-compose scale master=1 ubuntu=3`
Creates a master with 3 ubuntu minions

A few tools are available in ./aliases.
`source ./aliases`

Then you can shell into the master and run commands:
`master-shell`

## TODO ##
Add additional minion types.
Flush out mounting files to /srv/salt.
