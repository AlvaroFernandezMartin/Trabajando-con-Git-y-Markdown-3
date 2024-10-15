
## 1. Inicialización del proyecto

### Crear directorio y repositorio Git
```bash
mkdir /bloggalpon/
cd /bloggalpon/
git init
```
Se crea el directorio de trabajo `/bloggalpon/` y se inicializa un repositorio vacío con `git init`.

### Crear el archivo `index.htm`
```bash
touch index.htm
```

## 2. Añadir estructura básica a `index.htm`

### Añadir estructura básica HTML
El archivo `index.htm` contiene la siguiente estructura básica:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tarea 1.3</title>
</head>
<body>

    <section>
        <article>
            <h2>Título del post</h2>
            <p>Contenido del post.</p>
        </article>
    </section>
    
    <footer> Este es el footer</footer>
</body>
</html>
```

### Commit de la estructura básica
```bash
git add index.htm
git commit -m "Se crea el esqueleto básico del index.htm"
```

## 3. Añadir la cabecera al `head`

Se añade el contenido básico dentro del `<head>`:

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galpon</title>
</head>
```

### Commit de la cabecera
```bash
git add index.htm
git commit -m "Se añade la cabecera del index.htm"
```

## 4. Añadir estructura básica al `body`

Se añade la estructura básica dentro del `<body>`:

```html
<body>

    <section>
        <article>
            <h2>Título del post</h2>
            <p>Contenido del post.</p>
        </article>
    </section>
    
    <footer> Este es el footer</footer>
</body>
```

### Commit de la estructura básica del body
```bash
git add index.htm
git commit -m "Se añade la estructura básica del body"
```

## 5. Añadir estructura de la zona de posts

Añadir el contenido del `<section>` con un artículo básico:

```html
<section>
    <article>
        <h2>Título del post</h2>
        <p>Contenido del post.</p>
    </article>
</section>
```

### Commit de la estructura de la zona de posts
```bash
git add index.htm
git commit -m "Se añade toda la estructura de la zona de posts"
```

## 6. Crear archivo `style.css` y añadir estilos básicos

Se crea el archivo de estilos `style.css` y se añaden los estilos básicos para `html` y `body`:

```css
html, body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}
```

### Commit de los estilos básicos
```bash
git add style.css
git commit -m "Se añaden las CSS de html y de body"
```

## 7. Añadir estilos para elementos HTML5

Añadir estilos para los elementos `header`, `section`, `article`, `aside` y `footer`:

```css
header, section, article, aside, footer {
    display: block;
    margin: 10px;
}
```

### Commit de los estilos para elementos HTML5
```bash
git add style.css
git commit -m "Se añaden las CSS de varios elementos HTML5: header, section, article, aside y footer"
```

## 8. Añadir logotipo `logo.png`

Añadir el archivo de logotipo `logo.png` en el directorio raíz del proyecto.

### Commit del logotipo
```bash
git add logo.png
git commit -m "Se añade el logotipo de Pepsi"
```

## 9. Añadir estilos para la sección

Añadir estilos CSS para la sección:

```css
section {
    padding: 20px;
    background-color: #f4f4f4;
}
```

### Commit de los estilos de la sección
```bash
git add style.css
git commit -m "Se añaden las CSS de section"
```

## 10. Añadir estilos para el footer

Añadir estilos CSS para el footer:

```css
footer {
    text-align: center;
    padding: 10px;
    background-color: #333;
    color: white;
}
```

### Commit de los estilos del footer
```bash
git add style.css
git commit -m "Se añaden las CSS del footer"
```

## 11. Añadir estilos para `h1` y los enlaces

Añadir estilos CSS para los encabezados `h1` y los enlaces:

```css
h1 {
    font-size: 2em;
    color: #333;
}

a {
    color: #0066cc;
    text-decoration: none;
}
a:hover {
    text-decoration: underline;
}
```

### Commit de los estilos del `h1` y enlaces
```bash
git add style.css
git commit -m "Se añaden las CSS del H1 y de los enlaces"
```

## 12. Crear etiqueta `v1.0`

Crear una etiqueta `v1.0` para marcar el primer lanzamiento de la versión:

```bash
git tag v1.0
```

## 13. Crear rama de desarrollo

Crear una nueva rama llamada `desarrollo` para las nuevas tareas:

```bash
git checkout -b desarrollo
```

### 14. Reorganización de archivos

### Mover el logotipo a una nueva carpeta `images`
```bash
mkdir images
mv logo.png images/
git add images/logo.png
git commit -m "Se mueve el logotipo a la carpeta images"
```

### Mover el archivo CSS a una carpeta `CSS`
```bash
mkdir CSS
mv style.css CSS/
git add CSS/style.css
git commit -m "Se mueve la CSS a la carpeta CSS"
```

### Actualizar las referencias a las rutas de los archivos

Actualizar el archivo `index.htm` para apuntar al archivo CSS movido:

```html
<link rel="stylesheet" href="CSS/style.css">
```

Actualizar la referencia del logotipo en el archivo `style.css`:

```css
background-image: url('../images/logo.png');
```

### Commit de las referencias actualizadas
```bash
git add index.htm CSS/style.css
git commit -m "Se cambian las referencias a las CSS y a las imágenes al reorganizarlas en directorios"
```

## 15. Crear una rama de corrección de errores `bugfix`

Desde la rama `master`, crear una nueva rama llamada `bugfix`:

```bash
git checkout master
git checkout -b bugfix
```

### Quitar los comentarios en las CSS
Se eliminan los comentarios de las líneas punteadas en la barra derecha y el footer:

```css
/* Código eliminado */
//border-right: 1px dotted #ccc;
//border-top: 1px dotted #ccc;
```

### Commit de los ajustes de las líneas punteadas
```bash
git add CSS/style.css
git commit -m "Se introducen los punteados en la barra derecha y en el footer"
```

## 16. Introducir el título “Galpon”

Actualizar el archivo `index.htm` con el título "Galpon" en la página:

```html
<title>Galpon</title>
```

### Commit del título
```bash
git add index.htm
git commit -m "Se introduce el título en la página"
```

## 17. Pequeños ajustes en el footer

Cambiar el año en el footer de 2012 a 2014 y eliminar el símbolo de copyright `(c)`:

```html
<footer>
    <p>© 2014 Galpon. Todos los derechos reservados.</p>
</footer>
```

### Commit de los pequeños ajustes en el footer
```bash
git add index.htm
git commit -m "Se realizan pequeños ajustes en el footer"
```

## 18. Crear etiqueta `v1.1`

Crear una etiqueta `v1.1` para marcar el segundo lanzamiento:

```bash
git tag v1.1
```

## 19. Fusionar los cambios de la rama `bugfix` en `master`

Volver a la rama `master` y fusionar los cambios desde `bugfix`:

```bash
git checkout master
git merge bugfix
```

### Borrar la rama `bugfix`

Una vez fusionados los cambios, se puede eliminar la rama `bugfix`:

```bash
git branch -d bugfix
```

## 20. Fusionar los cambios de la rama `desarrollo` en `master`

Fusionar la rama `desarrollo` en `master`:

```bash
git merge desarrollo
```

### Resolver conflictos (si existen)

Si hay conflictos, se deben resolver manualmente, editar los archivos involucrados, y luego hacer `add` y `commit` de la resolución:

```bash
git add <archivo-conflicto>
git commit -m "Conflictos resueltos en la fusión de la rama desarrollo"
```

## 21. Crear etiqueta `v1.2`

Crear una etiqueta `v1.2` para marcar el tercer lanzamiento:

```bash
git tag v1.2
```
