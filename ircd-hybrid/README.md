#IRC server dockerfile

This dockerfile sets up a Debian container with ircd-hybrid, which can then be used for developing IRC bots etc.

##Build

In this folder, run:

    docker build -t user/imagename .

Example:

    docker build -t nikomo/irc .

##Run

Test the image:

    docker run -p 6667:6667 -t -i nikomo/irc

Run in the background:

    docker run -p 6667:6667 -d nikomo/irc

##Stop

Stop a container that's in the background with:

    docker stop containerid

Get container ID with:

    docker ps

Typing "docker stop" and hitting tab will autocomplete and bring up running containers if using some more advanced shells (zsh + oh-my-zsh works)