
---
### Propietario del Repositorio Principal:

- **Agregar un Submódulo:**
  ```bash
  git submodule add 'URL-del-Repositorio-Submódulo' ruta/del/submodulo
  ```

- **Inicializar y Actualizar Submódulos:**
  ```bash
  git submodule update --init --recursive
  ```

- **Verificar Estado:**
  ```bash
  git submodule status
  ```

- **Actualizar Submódulo:**
  ```bash
  git submodule update --remote
  ```

- **Eliminar Submódulo:**
  ```bash
  git submodule deinit -f ruta/del/submodulo
  git rm -f ruta/del/submodulo
  rm -rf .git/modules/ruta/del/submodulo
  ```

### Clonador del Repositorio con Submódulos:

- **Clonar con Submódulos:**
  ```bash
  git clone --recursive 'URL-del-Repositorio-Principal'
  ```

- **Inicializar y Actualizar Submódulos después de Clonar:**
  ```bash
  git submodule update --init --recursive
  ```

- **Actualizar Submódulos a la Última Versión:**
  ```bash
  git submodule update --remote
  ```
