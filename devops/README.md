## Deployment Steps. 

Copy the deploy.sh file to the home directory
```bash
cp deploy.sh ~/
```
Below are the links for samples for the default.yml file.
||
|---|
| [default-bap-client.yml](https://github.com/ONDC-Official/beckn-sandbox/blob/develop/config/samples/bap-client.yaml) |
| [default-bap-network.yml](https://github.com/ONDC-Official/beckn-sandbox/blob/develop/config/samples/bap-network.yaml) |
| [default-bpp-client.yml](https://github.com/ONDC-Official/beckn-sandbox/blob/develop/config/samples/bpp-client.yaml) |
| [default-bpp-network.yml](https://github.com/ONDC-Official/beckn-sandbox/blob/develop/config/samples/bpp-network.yaml) |




Edit the deploy.sh script and pass the correct **port number** and **default_yml** as per the requirement at the below line.

Also, add/change the cp with default.yml file in deploy.sh script.

To create the default.yml please follow the developer's guide.

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

