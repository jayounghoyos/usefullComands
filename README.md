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

EXecute
```bash
./anaconda.sh
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
python3 -m venv env
source env/bin/activate
pip freeze > requirements.txt
```
windows
```bash
python -m venv env
source env/bin/activate
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

#mongo for starting it 
```bash
sudo systemctl start mongod
```

# useful pip or just installs
fastapi
```bash
pip install fastapi
```
sqlalchemy
```bash
pip install sqlalchemy
```
psycopg2-binary
```bash
pip install psycopg2-binary
```

# ROS2 Commands for setup in new WSL ubuntu
```bash
locale  # Check current locale settings
sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8
locale  # Confirm updated locale settings
```

2. *Software Properties and Universe Repository*
```bash
sudo apt install software-properties-common
sudo add-apt-repository universe
```

3. *Curl Installation and ROS Key*
```bash
sudo apt update && sudo apt install curl -y
sudo curl -sSL https://raw.githubusercontent.com/ros... -o /usr/share/keyrings/ros-archive-keyring.gpg
```

4. *ROS2 Sources Configuration*
```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list (greater than**) /dev/null
```
Replace (greater than**) with actual symbol (youtube doesn't allow the symbol) 

5. *Update and Upgrade*
```bash
sudo apt update
sudo apt upgrade
```

6. *ROS Desktop Installation*
```bash
sudo apt install ros-humble-desktop
```

7. *ROS Environment Setup*
```bash
source /opt/ros/humble/setup.bash
```

8. *ROS2 Command Check*
```bash
ros2 
```

*ROS2 builds*
```bash
colcon build
colcon build --package-select my_py_pkg    #para hacer build a un paquete específico
```

*Create package (in python just rclcpy)*
```bash
ros2 pkg create my_cpp_pkg --build-type ament_cmake --dependencies rclcpp
```
OOP Python Code Template for Nodes
```bash
#!/usr/bin/env python3
import rclpy
from rclpy.node import Node
 
 
class MyCustomNode(Node): # MODIFY NAME
    def __init__(self):
        super().__init__("node_name") # MODIFY NAME
 
 
def main(args=None):
    rclpy.init(args=args)
    node = MyCustomNode() # MODIFY NAME
    rclpy.spin(node)
    rclpy.shutdown()
 
 
if __name__ == "__main__":
    main()
```
OOP C++ Code Template for Nodes
```bash
#include "rclcpp/rclcpp.hpp"
 
class MyCustomNode : public rclcpp::Node // MODIFY NAME
{
public:
    MyCustomNode() : Node("node_name") // MODIFY NAME
    {
    }
 
private:
};
 
int main(int argc, char **argv)
{
    rclcpp::init(argc, argv);
    auto node = std::make_shared<MyCustomNode>(); // MODIFY NAME
    rclcpp::spin(node);
    rclcpp::shutdown();
    return 0;
}
```

*Rename nodes in runtime(for example multi temperature sensors*
```bash
ros2 run my_py_pkg py_node --ros-args -r__node:=temperature_sensor1
```
