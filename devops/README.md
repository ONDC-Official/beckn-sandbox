## Deployment Setps. 

Copy the deploy.sh file to home directory
```bash
cp deploy.sh ~/
```
Edit the file and change the port number in default-bpp.yml or default-bap.yml file as per the requirement at below line.
default-client.yml 

To create the default.yml please follow the developers guide 

```bash
cp Dockerfile default-bap-client.yml default-bap-network.yml ~/beckn-sandbox
```

```bash
docker build -t bap-client --build-arg default_yml=default-bap-client.yml --build-arg port=5001 .
```

AND

```bash
docker build -t bap-client --build-arg default_yml=default-bap-network.yml --build-arg port=5000 .
```

