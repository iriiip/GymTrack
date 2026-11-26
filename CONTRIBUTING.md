# Normas de colaboración – TFG

## 1. Organización de ramas

Utilizaremos Git Flow simplificado con las siguientes ramas:

- `main`: contiene el código estable del proyecto.
- `develop`: rama principal de desarrollo e integración.
- `feature/*`: para desarrollar nuevas funcionalidades.
- `fix/*`: para corregir errores.

**Importante:** nunca se trabaja directamente sobre `main` ni `develop`.

## 2. Nombres de las ramas

Los nombres deben estar en inglés, en minúsculas y utilizando guiones para separar palabras.

Ejemplos:

```text
feature/user-login
feature/task-management
fix/login-validation
fix/database-connection
```

## 3. Commits

Utilizaremos Conventional Commits con el siguiente formato:

```text
tipo(ambito): descripcion
```

Tipos principales:

| Tipo | Uso |
|---|---|
| `feat` | Nueva funcionalidad |
| `fix` | Corrección de errores |
| `docs` | Documentación |
| `refactor` | Reestructuración de código |
| `test` | Pruebas |
| `chore` | Configuración y mantenimiento |

Ejemplos:

```text
feat(frontend): add login screen
feat(backend): implement user registration
fix(backend): correct user validation
docs: update readme
```

Los mensajes se escribirán en inglés, empezarán con minúscula y no terminarán en punto.

## 4. Flujo de trabajo

Para realizar cualquier tarea se seguirán estos pasos:

**1. Actualizar develop y crear una rama nueva:**

```bash
git switch develop
git pull origin develop
git switch -c feature/nombre-funcionalidad
```

Si se trata de una corrección, utilizaremos `fix/` en lugar de `feature/`.

**2. Realizar los cambios y crear commits:**

```bash
git add .
git commit -m "feat(frontend): add login screen"
```

**3. Subir la rama a GitHub:**

```bash
git push -u origin feature/nombre-funcionalidad
```

**4. Crear un Pull Request:**

Desde GitHub, crear un Pull Request seleccionando:

- Base: `develop`.
- Compare: nuestra rama `feature/*` o `fix/*`.

**5. Revisión e integración:**

Se revisará el Pull Request antes de aprobarlo e integrarlo en `develop`. No se deben integrar cambios directamente.

## 5. Normas generales

- No subir contraseñas, tokens ni credenciales.
- Comprobar que el código funciona antes de subirlo.
- Mantener los commits pequeños y descriptivos.
- Actualizar la rama de trabajo con `develop` cuando sea necesario.
- Eliminar las ramas de trabajo una vez integradas.
- No modificar código de otros compañeros sin coordinación.

**Todos los integrantes deberán seguir estas normas para mantener el repositorio organizado y facilitar el trabajo en equipo.**