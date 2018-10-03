## TL;DR
```
sudo mkdir /home/dock
sudo mkdir /home/dock/containers
sudo mkdir /home/dock/containers/confluence
```

```
docker run -v /home/dock/containers/confluence:/var/atlassian/application-data/confluence \
      --volume /etc/localtime:/etc/localtime:ro --volume /etc/timezone:/etc/timezone:ro \
      --name="confluence" -d -p 80:8090 -p 8091:8091  \
      atlassian/confluence-server
```
