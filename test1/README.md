runs nginx container with custom index.html file

### build:
```bash
docker build -t <name>:<tag> .
```
### run:
```bash
docker run --rm -it --name <container_name> -p <desired port>:80 <name>:<tag>
```