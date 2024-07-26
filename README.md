# This is for useful commands in my distributions or my projects

### Command list

```bash
mkdir folderName
```
```bash 
pip install something
```
```bash 
find nameOfFile
```
```bash 
sudo dpkg -i file_name.deb
```

### Instalations .sh

convert to executable 
```bash 
chmod +x nombre_del_script.sh
```
```bash 
chmod +x script_name.sh
```
`+x` adds executable permissions
```bash
sudo ./my_script.sh 
```

### Machine learning
- When you use conda, remember to add it to your PATH or select "yes" during the installation of the executable `.sh`
- Then, with Conda you can:
```bash
jupyter notebooks
```

### Jupyter
`shift + Enter` to run that specific cell
`Control + a + Enter` to run every cell

### Instalations .sh

### enviroment 
```bash 
python3 -m venv venv
source venv/bin/activate
pip freeze > requirements.txt
```
## Use the requirements to download the packages
```bash
pip install -r requirements.txt 
```
To desactivate the env 
```bash
deactivate
```
