# lucas
<p align="center">
    <img width="400"  src="http://ringtail-lucas.oss-cn-beijing.aliyuncs.com/lucas.png">
  <p align="center">etcd v3 key value browser</p>
</p>

etcd v3 api browser 

## Usage
```
NAME:
   lucas - A etcd v3 key/value browser implemented in go

USAGE:
   lucas [global options] command [command options] [arguments...]

VERSION:
   0.0.1

COMMANDS:
   run  run lucas web server

GLOBAL OPTIONS:
   --debug                          set debug mode to lucas
   --endpoints value                machine addresses in the cluster (default: "http://127.0.0.1:2379,http://127.0.0.1:4001")
   --cert-file value                identify HTTPS client using this SSL certificate file
   --key-file value                 identify HTTPS client using this SSL key file
   --ca-file value                  verify certificates of HTTPS-enabled servers using this CA bundle
   --help                           show help
   --version                        print the version
```

## Run in docker

// Simply use docker command
docker run -d -p 8088:8080  -v /etc/kubernetes/pki/etcd/:/etc/kubernetes/pki/etcd/ -e CA_FILE=/etc/kubernetes/pki/etcd/ca.pem -e CERT_FILE=/etc/kubernetes/pki/etcd/etcd-client.pem -e KEY_FILE=/etc/kubernetes/pki/etcd/etcd-client-key.pem -e ENDPOINTS="YOUR ENDPOINTS" registry.cn-hangzhou.aliyuncs.com/ringtail/lucas:0.0.1

// use yaml
kubectl create -f kubernetes-deployment.yaml (Add master node deployment affinity)

## Demo

<img src="http://ringtail-lucas.oss-cn-beijing.aliyuncs.com/demo/113671514107341_.pic_hd.jpg" width="90%"/>