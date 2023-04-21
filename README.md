¡Clonando y ejecutando el proyecto Laravel y Vue en pocos pasos!

1. Clonar el repositorio:
```
git clone https://github.com/seijas1235/PruebaMiddle.git
```

2. Navegar a la carpeta del proyecto:
```
cd PruebaMiddle
```

3. Instalar dependencias de Laravel:
```
composer install
```

4. Crear un archivo `.env` y configurar la conexión a la base de datos:
```
cp .env.example .env
```

5. Generar una nueva clave de aplicación de Laravel:
```
php artisan key:generate
```

6. Ejecutar migraciones de la base de datos:
```
php artisan migrate
```

7. Instalar las dependencias de Vue:
```
npm install
```

8. Compilar los assets de Vue: npm run dev


9. Ejecutar el servidor de Laravel: php artisan serve

10. Ver Vue en el navegador: http://localhost:8000
