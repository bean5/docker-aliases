# docker shortcut scripts

Mainly I find the dclean command to be helpful. It gets rid of killed containers and dangling containers (the pesky ones that appear as "none") when you run `docker images`.

It is also helpful for quick and dirty building/clean up of dockers. Ideal for development use only. Not advisable to use this for production purposes.

Following is a list of commands and what they do:

| Command		| Action 									| Notes									|
| d				| alias for docker							|										|
| db			| alias for `docker-compose build`			|										|
| dbr			| alias for `docker-compose run`			| Passes hostname to the container		|
| dbuild		| alias for `docker build .`				| Also names the image `temp`			|
| dbuildnocache	| same as dbuild, but ignores docker caches	|										|
| dclean		| calls drmstopped and drmdangling			| Great for space-constrained machines	|
| dcomp			| alias for `docker-compose` 				|										|
| dgip			| gets IP of a running docker container		| Requires container name as argument	|
| di			| alias for `docker iamges`					| 										|
| dkillall		| kill all running containers				| See also: dstopall					|
| dps			| provides ps info for container			| Requires container name as argument	|
| drm			| alias for `docker rm`						| 										|
| drmi			| alias for `docker rm`						| 										|
| drmdangling	| removes dangling images					| You know, the ones called "none"		|
| drmstopped	| removes stopped containers				| Great for space-constrained machines	|
| drun			| runs the container that is called `temp`	| e.g.: dbuild && drun					|
| drun8080		| runs container with port -p 80:80			| See also: drunforward					|
| drunforward	| runs container with port -p 80:80			| See also: drun8080					|
| dstopall		| stops all running containers				| More graceful than dkillall			|
| dtagTemp		| quick tagging of container called `temp`	| e.g.: dbuild && tagLast LocalService	|



## Set Up
To set up do something like this in your bashrc file: `PATH=$PATH:~/workspace/scripts-docker/`. The change should take once you open a new shell.
