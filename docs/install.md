# Instalación de Python 3.12.7

## Requisitos previos

- Asegúrate de tener privilegios de administrador en tu sistema.
- Conexión a Internet para descargar los archivos necesarios.

## Instalación en Ubuntu

1. **Actualizar el sistema:**

    ```sh
    sudo apt update
    sudo apt upgrade
    ```

2. **Instalar dependencias necesarias:**

    ```sh
    sudo apt install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev curl libbz2-dev
    ```

3. **Descargar Python 3.12:**

    ```sh
    cd /tmp
    curl -O https://www.python.org/ftp/python/3.12.0/Python-3.12.0.tgz
    ```

4. **Extraer el archivo descargado:**

    ```sh
    tar -xf Python-3.12.0.tgz
    ```

5. **Compilar e instalar Python:**

    ```sh
    cd Python-3.12.0
    ./configure --enable-optimizations
    make -j $(nproc)
    sudo make altinstall
    ```

6. **Verificar la instalación:**

    ```sh
    python3.12 --version
    ```

## Instalación en Windows

1. **Descargar el instalador de Python 3.12:**

    - Ve a la página oficial de Python: [https://www.python.org/downloads/release/python-3120/](https://www.python.org/downloads/release/python-3120/)
    - Descarga el instalador adecuado para tu sistema (32-bit o 64-bit).

2. **Ejecutar el instalador:**

    - Abre el archivo descargado.
    - Marca la opción "Add Python 3.12 to PATH".
    - Selecciona "Customize installation".

3. **Personalizar la instalación:**

    - Asegúrate de que todas las opciones estén seleccionadas y haz clic en "Next".
    - En la siguiente pantalla, selecciona "Install for all users" y toma nota del directorio de instalación.
    - Haz clic en "Install".

4. **Verificar la instalación:**

    - Abre una ventana de Command Prompt (cmd) y ejecuta:

    ```sh
    python --version
    ```

## Configuración adicional

### Instalación de pip

`pip` debería instalarse automáticamente con Python 3.12. Puedes verificarlo ejecutando:

```sh
pip --version