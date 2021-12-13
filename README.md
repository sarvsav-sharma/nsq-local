# nsq-local
To run nsq in cluster locally

# To start run below command
```shell
docker-compose up -d
```

And add the below  `/etc/hosts` file
```text
#NSQ localsetup
127.0.0.1 weave-nsq-nsqd1
127.0.0.1 weave-nsq-nsqd2
127.0.0.1 weave-nsq-nsqd3
```

# To create topics
```shell
curl -d "Writing to first node" http://localhost:4151/pub?topic=WeaveTopic
curl -d "Writing to second node" http://localhost:4251/pub?topic=WeaveTopic
curl -d "Writing to third node" http://localhost:4351/pub?topic=WeaveTopic
```

# To bring down the cluster
```shell
docker-compose down
```

# Admin UI available
```
http://127.0.0.1:4161/
```
