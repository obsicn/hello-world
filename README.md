# About this Repo

This is the Git repo of the Docker [official image](https://docs.docker.com/docker-hub/official_repos/) for [hello-world](https://registry.hub.docker.com/_/hello-world/). See [the Docker Hub page](https://registry.hub.docker.com/_/hello-world/) for the full readme on how to use this Docker image and for information regarding contributing and issues.

The full readme is generated over in [docker-library/docs](https://github.com/docker-library/docs), specifically in [docker-library/docs/hello-world](https://github.com/docker-library/docs/tree/master/hello-world).

See a change merged here that doesn't show up on the Docker Hub yet? Check [the "library/hello-world" manifest file in the docker-library/official-images repo](https://github.com/docker-library/official-images/blob/master/library/hello-world), especially [PRs with the "library/hello-world" label on that repo](https://github.com/docker-library/official-images/labels/library%2Fhello-world). For more information about the official images process, see the [docker-library/official-images readme](https://github.com/docker-library/official-images/blob/master/README.md).

---

-	[Travis CI:  
	![build status badge](https://img.shields.io/travis/docker-library/hello-world/master.svg)](https://travis-ci.org/docker-library/hello-world/branches)

<!-- THIS FILE IS GENERATED BY https://github.com/docker-library/docs/blob/master/generate-repo-stub-readme.sh -->



[root@devops-srv hello-world]# make
gcc -static -Os -nostartfiles -fno-asynchronous-unwind-tables -o 'hola-mundo/hello' -D DOCKER_IMAGE='"hola-mundo"' -D DOCKER_GREETING="\"$(cat 'hola-mundo/greeting.txt')\"" 'hello.c'
/usr/bin/ld: cannot find -lc
collect2: error: ld returned 1 exit status
make: *** [hola-mundo/hello] Error 1

原因是本地没有安装静态库
[root@devops-srv hello-world]# yum install glibc-static.x86_64

Loaded plugins: fastestmirror, langpacks
base                                                                                                                                  | 3.6 kB  00:00:00     
dockerrepo                                                                                                                            | 2.9 kB  00:00:00     
extras              
