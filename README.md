# CableTelco / TV MAX



Nota: los datos y usuarios Auth del proyecto origen no están incluidos en este paquete. Requieren acceso al proyecto origen para migrarlos.


Corrección adicional: `initializeSession` usa `maybeSingle()` y distingue entre un error de consulta y un usuario Auth sin perfil en `public.perfiles`. El Service Worker se actualizó a v13 para evitar servir una copia antigua de `app.js`.

Los asesores ya no tienen registro público: la pantalla de alta fue eliminada. Los asesores se crean únicamente desde `Usuarios` dentro del panel del administrador. La Edge Function `admin-users` crea los usuarios con el correo confirmado automáticamente.

## Zonas oficiales
El sistema utiliza estas cinco zonas para los asesores: Caucasia, San Marcos, La Apartada, Montelíbano y Buenavista. El administrador las selecciona desde un desplegable al crear o editar un asesor; la Edge Function también valida el valor.
