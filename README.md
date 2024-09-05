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
### App Image
```bash 
chmod +x your_appimage_file.AppImage
```
Run App Image
```bash
./your_appimage_file.AppImage
```
### Machine learning
- When you use conda, remember to add it to your PATH or select "yes" during the installation of the executable `.sh`
- Then, with Conda you can:
```bash
jupyter notebooks
```
-Train YOLO model
```bash
!python train.py --data data.yaml --weights yolov5s.pt --batch-size 8 --name Model --img 640 --epochs 150
```
-Resume Training YOLO V5 Model
```bash
python train.py --data data.yaml --weights best.pt
```
- In the new update of opencv and YoloV5. There is change in command  to export model as .onnx. Use below updated command to export model
```bash
python export.py --weights runs/train/Model/weights/best.pt --include onnx --simplify --opset 12
```
```bash
pip install opencv-python
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

## Install Doom
```bash
sudo apt-get install chocolate-doom
```
run with:
```bas
chocolate-doom
```

# wall paper POP_os
```bash
sudo add-apt-repository ppa:variety/stable
sudo apt-get update
sudo apt-get install variety
```
