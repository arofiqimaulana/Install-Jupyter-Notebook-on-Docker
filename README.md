# Install Jupyter Notebook on Docker
Berikut ini merupakan cara instalasi Jupyter Notebook menggunakan Docker via docker compose. Instalasi menggunakan docker compose lebih mudah digunakan karena kita bisa menuliskan konfigurasi kita di file .yml.

## Command
* ```docker-compose up``` mounts the directory and starts the container
* ```docker-compose down``` destroys the container

## Compose file (.yml)
```
version:                "3"
services:
  datascience-notebook:
      image:            jupyter/datascience-notebook
      volumes:
        - C:/Users/LENOVO:/home/jovyan/work
      ports:
        - 8888:8888
      container_name:   datascience-notebook-container
```

