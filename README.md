# Clonar el repositorio

## Clonar el repositorio
Para clonar este repositorio con Git, usa el siguiente comando:

```bash
git clone https://github.com/Laura250212/Practica.git
```

Luego, entra en la carpeta con:

```bash
cd Practica
```

Para actualizar los cambios más recientes, ejecuta:

```bash
git pull origin main
```
*(Si la rama principal es `master`, usa `git pull origin master`).*

---

## Descargar el repositorio sin clonarlo
Si solo quieres descargar el código sin el historial de Git, usa uno de los siguientes comandos:

### **Con `wget`**
```bash
wget https://github.com/Laura250212/Practica/archive/refs/heads/main.zip
```

### **Con `curl`**
```bash
curl -L -o Practica.zip https://github.com/Laura250212/Practica/archive/refs/heads/main.zip
```

Para extraerlo después:
```bash
unzip Practica.zip && rm Practica.zip
