#IRC server dockerfile

This dockerfile sets up a Debian container with ircd-hybrid, which can then be used for developing IRC bots etc.

#Getting it

This Git repository contains the dockerfile, but this is also available directly from the Docker repository:

    docker pull nikomo/ircd-hybrid

Or you can build it

##Build

In this folder, run:

    docker build -t user/imagename .

Example:

    docker build -t nikomo/ircd-hybrid .

##Run

Test the image:

    docker run -p 6667:6667 -t -i nikomo/ircd-hybrid

Run in the background:

    docker run -p 6667:6667 -d nikomo/ircd-hybrid

##Stop

Stop a container that's in the background with:

    docker stop containerid

Get container ID with:

    docker ps

Typing "docker stop" and hitting tab will autocomplete and bring up running containers if using some more advanced shells (zsh + oh-my-zsh works)