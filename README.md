# Install Jupyter Notebook on Docker
Berikut ini merupakan cara instalasi Jupyter Notebook menggunakan Docker via docker compose. Instalasi menggunakan docker compose lebih mudah digunakan karena kita bisa menuliskan konfigurasi kita di file .yml.


## Macam Image 
Terdapat beberapa macam image yang bisa kita gunakan yaitu

1. jupyter/minimal-notebook 
2. jupyter/datascience-notebook
3. jupyter/scipy-notebook
4. jupyter/all-spark-notebook


## Compose file (.yml) Example
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

## Langkah Instalasi
1. Letakkan file compose .yml di suatu folder
2. Buka terminal (CMD) dan ketikkan ``` docker-compose up ```