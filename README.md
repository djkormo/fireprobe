```
docker-compose up -d
```
```
docker-compose ps 
```
<pre>
Name                   Command               State                                         Ports                                       
--------------------------------------------------------------------------------------------------------------------------------------------
fireprobe        /bin/sh -c python3 /app/bi ...   Up      0.0.0.0:9113->9113/tcp,:::9113->9113/tcp, 0.0.0.0:9114->9114/tcp,:::9114->9114/tcp
ooklaspeedtest   ./OoklaServer start              Up      0.0.0.0:5060->5060/tcp,:::5060->5060/tcp, 0.0.0.0:8080->8080/tcp,:::8080->8080/tcp
rfb-testserver   npm start                        Up      0.0.0.0:8888->8888/tcp,:::8888->8888/tcp   
</pre>


```
docker-compose logs
```
