# Practica - Repositorio de Práctica

Este repositorio contiene el código fuente del proyecto. A continuación, se detallan las instrucciones para clonar, descargar y colaborar en el repositorio, así como cómo manejar conflictos al fusionar cambios.

---

## Clonar el Repositorio con Git

Para trabajar con el historial completo del repositorio y poder contribuir al proyecto, sigue estos pasos:

### 1. Clona el repositorio:
Ejecuta el siguiente comando en tu terminal para clonar el repositorio:

```bash
git clone https://github.com/Laura250212/Practica.git
```

### 2. Accede a la carpeta del proyecto:
Una vez clonado, ingresa a la carpeta del repositorio con:

```bash
cd Practica
```

### 3. Actualiza el repositorio:
Para obtener los cambios más recientes desde el repositorio remoto, ejecuta:

```bash
git pull origin main
```

Nota: Si la rama principal del repositorio es `master` en lugar de `main`, usa el siguiente comando:

```bash
git pull origin master
```

---

## Descargar el Repositorio sin Clonarlo

Si solo necesitas descargar el código fuente sin el historial de Git, puedes hacerlo de las siguientes maneras:

### Usando `wget`:
1. Descarga el repositorio como un archivo ZIP:

```bash
wget https://github.com/Laura250212/Practica/archive/refs/heads/main.zip
```

2. Extrae el archivo ZIP:

```bash
unzip main.zip
```

3. (Opcional) Elimina el archivo ZIP después de extraerlo:

```bash
rm main.zip
```

### Usando `curl`:
1. Descarga el repositorio como un archivo ZIP:

```bash
curl -L -o Practica.zip https://github.com/Laura250212/Practica/archive/refs/heads/main.zip
```

2. Extrae el archivo ZIP:

```bash
unzip Practica.zip
```

3. (Opcional) Elimina el archivo ZIP después de extraerlo:

```bash
rm Practica.zip
```

---

## Estructura del Repositorio

Una vez que hayas clonado o descargado el repositorio, encontrarás la siguiente estructura de carpetas y archivos:

```
Practica/
├── README.md          # Este archivo
├── src/               # Código fuente del proyecto
├── docs/              # Documentación del proyecto
└── ...                # Otros archivos y carpetas
```

---

## Manejo de Conflictos al Hacer Merge

Cuando dos personas trabajan en el mismo archivo o directorio, es posible que surjan conflictos al intentar fusionar (merge) los cambios. Git intentará fusionar automáticamente, pero si los cambios son incompatibles (por ejemplo, ambas personas editaron la misma línea de un archivo), se producirá un conflicto de merge.

### ¿Qué sucede durante un conflicto de merge?

Cuando se produce un conflicto de merge, Git no puede fusionar automáticamente los cambios y te notificará que ha ocurrido un conflicto. Los pasos para resolverlo son los siguientes:

1. **Git te indica el conflicto**: 
   Git marcará los archivos en conflicto y añadirá marcas en el archivo para mostrar las diferencias:

   ```plaintext
   <<<<<<< HEAD
   Cambios de Persona 1
   =======
   Cambios de Persona 2
   >>>>>>> branch-name
   ```

   Los cambios de Persona 1 están en la parte superior (después de `<<<<<<< HEAD`) y los de Persona 2 están en la parte inferior (después de `=======`).

2. **Resuelve el conflicto**:
   Tienes que decidir qué cambios mantener. Puedes:
   - Mantener los cambios de una persona.
   - Fusionar los cambios de ambas personas.
   Elimina las marcas de conflicto (`<<<<<<<`, `=======`, `>>>>>>>`) después de resolver el conflicto.

3. **Añadir los archivos resueltos**:
   Una vez que hayas resuelto los conflictos, añade los archivos modificados al área de preparación con:

   ```bash
   git add <archivo>
   ```

4. **Realizar un commit de la resolución**:
   Después de resolver los conflictos y añadir los archivos, realiza un commit para registrar la resolución del conflicto:

   ```bash
   git commit
   ```

   Git generará automáticamente un mensaje de commit para el merge (resolución de conflictos).

5. **Hacer push**:
   Finalmente, después de realizar el commit, sube los cambios al repositorio remoto con:

   ```bash
   git push origin main
   ```

---

## Consejos para Evitar Conflictos

Si quieres entender mejor cómo manejar los conflictos de merge, puedes revisar el siguiente repositorio como referencia:

[Conflictos Merge - Mi otro repositorio](https://github.com/rsensomontojo/Conflictos_merge)

---

¡Feliz codificación y colaboración! 😊
