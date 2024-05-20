# Fedele QRCode Extension
Esta extension es un fork de https://github.com/netbox-community/netbox-qrcode

## Creación del Fork
Para futuras actualizaciones de la Extensión, si se desea realizar un nuevo fork, se debe realizar el siguiente procedimiento:

1. Hacer el Fork
2. Añadir remoto: 
  
  ```
  git remote add upstream [GitHub repo original]
  ```

3. Obtener tags: 
  ```
  git fetch upstream --tags
  ```

4. Ir a rama main:
  ```
  git checkout main
  ```

5. Reiniciar rama main con el tag a utilizar:

  ```
  git reset --hard tags/nombre-del-tag  
  ```

6. Pushear cambios:
  ```
  git push --force origin main
  ```

## Instalación

1. Cambiar netbox_qrcode por fedele_qrcode en ```__init__.py``` y en ```setup.py```

2. Cambiar nombre de carpeta de proyecto a ```fedele_qrcode```

3. Cambiar nombre de carpeta ```/fedele_qrcode/templates/netbox_qrcode``` a ```/fedele_qrcode/templates/fedele_qrcode```

4. Con ```Ctrl + Shift + H``` reemplazar ```netbox_qrcode``` por ```fedele_qrcode``` en TODOS lados

5. Con ```Ctrl + Shift + H``` reemplazar ```netbox-qrcode``` por ```fedele-qrcode``` en TODOS lados

6. Activar entorno virtual: 
```
source /opt/o4n/O4N_FEDELE_SOURCE/venv/bin/activate
```

7. Instalar Extensión: 
  ```
  python setup.py develop
  ```

8. En ```configuration.py``` de Fedele agregar:
  ```
  PLUGINS = ["fedele_qrcode"]
  ```

