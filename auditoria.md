# Auditoría de Seguridad y Funcionalidad del Sistema Financiero

Este documento describe las implementaciones de seguridad y funcionalidad para cumplir con los requisitos del sistema financiero solicitado.

---

## 1. Registro de Clientes con Contraseñas Encriptadas

- **Descripción**: Las contraseñas de los clientes se encriptan usando `password_hash` con el algoritmo `BCRYPT`.
- **Motivo**: Esta técnica de encriptación permite almacenar contraseñas de manera segura, protegiendo la información confidencial de los usuarios.
- **Ubicación en el código**: Implementado en `register.php`.

### Código de Ejemplo
```php
$hashedPassword = password_hash($password, PASSWORD_BCRYPT);
