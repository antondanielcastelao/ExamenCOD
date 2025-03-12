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
Empezamos por los **commits de la branch datos**
```bash
git checkout datos
# proceso para hacer un commit (repetido varias veces)
git add .\scr\Datos.java
git commit -m "conexion base de datos"
```
Repetimos el proceso y hacemos un par de commits en la branch interface
```bash
git checkout interface
# proceso para hacer un commit (repetido varias veces)
git add .\scr\Interface.java
git commit -m "terminada ventana interfaz"
```
Para hacerlo más interesante, vamos a hacer un cambio en main y harémos un **rebase** en ambas ramas
```bash
git checkout main
# hacemos el cambio en la clase Main...
git add .\scr\Main.java
git commit -m "cambio de la funcion principal"

# vamos a las otras ramas y hacemos el rebase
git checkout interface
git rebase main

git checkout datos
git rebase main

git checkout readme
git rebase main
```
Terminamos el desarrollo de la conexion con la base de datos, por lo que **mezclamos la rama con nuestra rama principal**
```bash
git checkout main
git merge datos

git commit -m "implementacion rama datos"
```