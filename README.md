# Manage and Monitor the Docker Containers with Dry Tool 



## Tested Infrastructure

<table class="tg">
  <tr>
    <th class="tg-yw4l"><b>Platform</b></th>
    <th class="tg-yw4l"><b>Number of Instance</b></th>
    <th class="tg-yw4l"><b>Reading Time</b></th>
    
  </tr>
  <tr>
    <td class="tg-yw4l"><b> Play with Docker</b></td>
    <td class="tg-yw4l"><b>1</b></td>
    <td class="tg-yw4l"><b>5 min</b></td>
    
  </tr>
  
</table>

## Pre-requisite

- Create an account with [DockerHub](https://hub.docker.com)
- Open [PWD](https://labs.play-with-docker.com/) Platform on your browser 
- Click on **Add New Instance** on the left side of the screen to bring up Alpine OS instance on the right side





```
[node1] (local) root@192.168.0.33 ~
$ docker pull busybox
Using default tag: latest
latest: Pulling from library/busybox
57c14dd66db0: Pull complete
Digest: sha256:7964ad52e396a6e045c39b5a44438424ac52e12e4d5a25d94895f2058cb863a0
Status: Downloaded newer image for busybox:latest

[node1] (local) root@192.168.0.33 ~
$ docker pull hello-world
Using default tag: latest
latest: Pulling from library/hello-world
1b930d010525: Pull complete
Digest: sha256:2557e3c07ed1e38f26e389462d03ed943586f744621577a99efb77324b0fe535
Status: Downloaded newer image for hello-world:latest

[node1] (local) root@192.168.0.33 ~
$ docker run -t -d busybox
7c96cde9894fd9ff42d1c3638cad65cf306cb2757b3925a925f4d421a510a79f

[node1] (local) root@192.168.0.33 ~
$ docker run -t -d hello-world
7a4198a31f61c380ddbe3b06eeb313da74de3d232727b0325937434900e8be8d
[node1] (local) root@192.168.0.33 ~
$ docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS      PORTS               NAMES
7c96cde9894f        busybox             "sh"                3 minutes ago       Up 3 minutes                          romantic_greider
[node1] (local) root@192.168.0.33 ~
$ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS             PORTS               NAMES
7a4198a31f61        hello-world         "/hello"            3 minutes ago       Exited (0) 3 minutes ago                       stupefied_tu
7c96cde9894f        busybox             "sh"                3 minutes ago       Up 3 minutes                                 romantic_greider
[node1] (local) root@192.168.0.33 ~
$ docker run -it -v /var/run/docker.sock:/var/run/docker.sock moncho/dry
Unable to find image 'moncho/dry:latest' locally
latest: Pulling from moncho/dry
4fe2ade4980c: Pull complete
e9c4f9f2a7e3: Pull complete
28bab79b92a9: Pull complete
Digest: sha256:ad57f88f39fd910cc42e9416594dd2cf92ae561ddd914fd1c333f989a8d5bd4b
Status: Downloaded newer image for moncho/dry:latest

```
## Contributor - 

Sangam biradar - smbiradar14@gmail.com -https://engineitops.github.io 

