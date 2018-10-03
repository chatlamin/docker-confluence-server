
```
sudo mkdir -p /home/docker/confluence
```

```
docker run -v /home/docker/confluence:/var/atlassian/application-data/confluence \
      --volume /etc/localtime:/etc/localtime:ro --volume /etc/timezone:/etc/timezone:ro \
      --name="confluence" -d -p 8090:8090 -p 8091:8091  \
      atlassian/confluence-server
```
