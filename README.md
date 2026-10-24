# chesslens

<div align="center">
    <img width="476" height="868" alt="image" src="https://github.com/user-attachments/assets/369d0637-1995-4e81-898b-68965a876f3b" />

</div>

## Running the application
```
$ sudo docker run -dit -p <PORT>:87 --name <CONTAINER-NAME> yashindane/chesslens:v1 --apikey="<OPENAI-API-KEY>"
```

Port mapping for reaching Docker container hosted on WSL -

```
Powershell

> netsh interface portproxy add v4tov4 listenport=<PORT> listenaddress=0.0.0.0 connectport=<PORT> connectaddress=<eth0 IP of WSL>
> netsh advfirewall firewall add rule name="Flask PORT" dir=in action=allow protocol=TCP localport=<PORT>
```

Live Container logs -
```
$ sudo docker logs -f <CONTAINER-ID>
```
