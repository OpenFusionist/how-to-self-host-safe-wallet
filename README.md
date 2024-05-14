# How to self host safe wallet



## Requirements

1. CPU     2 Cores/ 4 vCPU
2. RAM    8GB
3. DISK    100GB SSD



## Using Docker

**Prerequisite:** Install [Docker Engine](https://docs.docker.com/engine/) and [Docker Compose](https://docs.docker.com/compose/install)

**Important Note:** If you followed the guide some time ago, it's recommended to clean the existing data:

- Remove docker volumes: `docker compose -f docker-compose.core.yml -f docker-compose.tx.yml rm -v`.
- Remove `./data` folder, that holds the database.



Once Docker is installed on your system, run the following command to host your safe wallet:

```shell
git clone https://github.com/OpenFusionist/how-to-self-host-safe-wallet.git
cd how-to-self-host-safe-wallet/safewallet
cp .env.sample .env

# Modify .env before running this command.
docker compose -f docker-compose.core.yml -f docker-compose.tx.yml up -d
```
