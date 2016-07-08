h2. Know your machine IP (only when using docker-machine)

``` shell
$ docker-machine ip
```

h2. add At least 2 hosts

in your hosts file
/etc/hosts
or
C:/windows/System32/drivers/etc/hosts

add 
YOURIP project1.dev
YOURIP project2.dev

h2. Build and up

``` shell
$ docker-compose -f main.yml up
```

or with -d to hide any message and let the containers run in background

``` shell
$ docker-compose -f main.yml up -d
```

h2. Where ?

Nginx is configured this way : 
Ask project1.dev and it will load html/project/
Ask bar.dev and it will load html/bar/

by default come with project1 and project2

to manage your databases add 8080 port to any project url
ex: project1.dev:8080