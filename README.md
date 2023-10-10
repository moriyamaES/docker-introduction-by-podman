# docker-introduction-udemy-by-podman
 駆け出しエンジニアのためのDocker入門（Podmanで実行）

## podman run

- 以下のコマンドを実行

    ```sh
    podman run hello-world
    Resolved "hello-world" as an alias (/etc/containers/registries.conf.d/000-shortnames.conf)
    Trying to pull quay.io/podman/hello:latest...
    Getting image source signatures
    Copying blob d08b40be6878 done  
    Copying config e2b3db5d4f done  
    Writing manifest to image destination
    !... Hello Podman World ...!

            .--"--.           
        / -     - \         
        / (O)   (O) \        
    ~~~| -=(,Y,)=- |         
        .---. /`  \   |~~      
    ~/  o  o \~~~~.----. ~~   
    | =(X)= |~  / (O (O) \   
    ~~~~~~~  ~| =(Y_)=-  |   
    ~~~~    ~~~|   U      |~~ 

    Project:   https://github.com/containers/podman
    Website:   https://podman.io
    Documents: https://docs.podman.io
    Twitter:   @Podman_io
    ```

## podman ps

- 以下のコマンドを実行

    ```sh
    podman ps -a
    CONTAINER ID  IMAGE                        COMMAND               CREATED         STATUS                     PORTS       NAMES
    e9320ffb2bb9  quay.io/podman/hello:latest  /usr/local/bin/po...  14 minutes ago  Exited (0) 14 minutes ago              focused_ritchie
    ```

## podman run --rm

    ```sh
    podman ps -a
    CONTAINER ID  IMAGE       COMMAND     CREATED     STATUS      PORTS       NAMES
    [kazuhiro@localhost ~]
    $ podman run --name uchida --rm hello:latest 
    !... Hello Podman World ...!

            .--"--.           
        / -     - \         
        / (O)   (O) \        
    ~~~| -=(,Y,)=- |         
        .---. /`  \   |~~      
    ~/  o  o \~~~~.----. ~~   
    | =(X)= |~  / (O (O) \   
    ~~~~~~~  ~| =(Y_)=-  |   
    ~~~~    ~~~|   U      |~~ 

    Project:   https://github.com/containers/podman
    Website:   https://podman.io
    Documents: https://docs.podman.io
    Twitter:   @Podman_io
    [kazuhiro@localhost ~]
    $ podman ps -a
    CONTAINER ID  IMAGE       COMMAND     CREATED     STATUS      PORTS       NAMES
    ```

