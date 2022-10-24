# STREAMLIT SERVICE

## Docker Deploy

Se crea la imagen
```
docker build -t streamlit .
```

Se revisa que exista la imagen "streamlit"
```
docker images
```

Crear el servicio en localhost para pruebas
```
docker run -p 8501:8501 --name streamlit --env-file=src/components/.env streamlit env
```

Se crea el servicio para producción
```
docker run -p 8501:8501 --name streamlit --env-file=src/components/.env.production streamlit env
```