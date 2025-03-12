# Examen COD Anton Davila
## 1er Paso: Crear las ramas
```bash
# nos aseguramos de que esta la rama main creada
git branch
# empezamos a crear
git checkout -b datos
git checkout -b interface
git checkout -b readme
```
## 2o Paso: Commits del desarrollo de la release
Empezamos por los commits de la branch datos
```bash
git checkout datos
# proceso para hacer un commit (repetido varias veces)
git add .\scr\Datos.java
git commit -m "conexion base de datos"
```