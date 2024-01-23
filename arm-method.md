# X86-64 Architecture

This method uses a databse with an ARM architecture, which might be faster to run.

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