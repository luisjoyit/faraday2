primero descargas el wsl ubuntu


entramos al terminal del wsl ubuntu 
 Instalar sus  dependencias
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
    libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
    libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python3-openssl \
    pkg-config postgresql postgresql-contrib redis-server

```

Instalar y Configurar pyenv

```bash
curl https://pyenv.run | bash
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"
source ~/.bashrc
```
Instalar Python 3.

```bash
pyenv install 3.10.12
```

Crear y activar un entorno virtual

```bash
pyenv virtualenv 3.10.12 py-ia-project
pyenv local py-ia-project
```
actualizamos
```bash
python -m pip install --upgrade pip
```
instalamso el farady clip
```bash
pip install faraday-cli
```
inicamos copiasmo la url de faday server y la contraseña y el usuario sacamso el faray en docker
```bash
export FARADAY_SERVER=http://localhost:5985
faraday-cli auth
```
entrar
```bash
faraday-cli
```


ver todos los trabjos 
```bash
workspace list
```

crear 
```bash
workspace create (nombre del nuevo trabajo)
```

entar 
```bash
workspace select (nombre del trabajo)
```

subir reporte 

faraday import --file (ruta del reporte
)

