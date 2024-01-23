# X86-64 Architecture

This method uses a databse with an ARM architecture, which might be faster to run.
**But it has never worked correctly.**

## Instalation:
Get docker

Clone this repository and navigate into it:
```sh
git clone -b 19c-arm-slim https://github.com/marcelo-ochoa/oci-oracle-free 
cd oci-oracle-free
```

Build the image of the slim version:
```sh
docker buildx build --build-arg BUILD_MODE=SLIM -t oracle/database:19.3.0-ee-slim -f Dockerfile.193 .
```

To run the image, run:
```
docker run -d --name test19c \
-e ORACLE_PASSWORD=Oracle_2023 \
-e APP_USER=scott \
-e APP_USER_PASSWORD=tiger \
-e ORACLE_PASSWORD=<password> \
-p 1521:1521 \
oracle/database:19.3.0-ee-slim
```



For more information go to [https://github.com/marcelo-ochoa/oci-oracle-free](https://github.com/marcelo-ochoa/oci-oracle-free)
