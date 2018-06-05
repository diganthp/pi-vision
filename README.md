# PI V.I.S.I.O.N: Portable Infinitesimal Video Input Signal Processed Intelligent Object Naming
This project is based on SqueezeDet by @Bichen Wu. To the work done by bichenWuUCB, our team added a new feature of determining the distance of the object in real time using the principle of triangular similarity. Using distance as a parameter we could vary the intensity of the haptic motor to alert the user about how near he/she is to the object. We also Integrated Google Assistant which will help the user to get the information he needs and is triggered using a push button.  The whole project was carried out using a Raspberry Pi 3B/3B+. This project was solely based to help the visually impaired people to get through everyday life in a easy way. 
## Requirements:
* easydict
* joblib
* numpy
* python openCV
* pillow
* tensorflow (tensorflow 1.4 recommended)

## Installation:

The following instructions are written for Linux-based distros.

- Clone the PI VISION repository:

  ```Shell
  git clone https://github.com/diganthp/pi-vision.git
  ```
  Let's call the top level directory of pi-vision `$SQDT_ROOT`. 

- (Optional) Setup your own virtual environment.

  1. The following assumes `python` is the Python2.7 executable. Navigate to your user home directory, and create the virtual environment there.
  
    ```Shell
    cd ~
    virtualenv env --python=python
    ```
    
  2. Launch the virtual environment.
  
    ```Shell
    source env/bin/activate
    ```
    
- Use pip to install required Python packages:
    
    ```Shell
    pip install -r requirements.txt
    ```
## Demo on Laptop running Ubuntu 16.04:
- Download SqueezeDet model parameters from [here](https://www.dropbox.com/s/a6t3er8f03gdl4z/model_checkpoints.tgz?dl=0), untar it, and put it under `$SQDT_ROOT/data/` If you are using command line, type:

  ```Shell
  cd $SQDT_ROOT/data/
  wget https://www.dropbox.com/s/a6t3er8f03gdl4z/model_checkpoints.tgz
  tar -xzvf model_checkpoints.tgz
  rm model_checkpoints.tgz
  ```


- Now we can run the demo. To detect the sample image `$SQDT_ROOT/data/sample.png`,

  ```Shell
  cd $SQDT_ROOT/
  python ./src/demo.py
  ```
  If the installation is correct, the detector should generate this image: ![alt text](https://github.com/diganthp/pi-vision/blob/master/Images/output%201%20.png)
  
  A huge thanks to @BichenWuUCB and team for thier work on squeezeDet.
  Link to repo: [squeezeDet](https://github.com/BichenWuUCB/squeezeDet)
  
## Implementation on Raspberry PI:
### Software Requirements: 
* easydict
* joblib
* numpy
* python openCV
* pillow
* tensorflow (tensorflow 1.1 above recommended)
* python 3.4 (This version of python is recommended since there is no support for tensorflow 1.1 for python 3.5 or python 3.6)
* Google Assistant Installation on Raspberry Pi. Installation of the Google Assistant can be at [Google Developers - Installation of the Google Assistant on Raspberry Pi 3](https://developers.google.com/assistant/sdk/guides/library/python/)

### Hardware Requirements:
* LED
![alt text](https://github.com/diganthp/pi-vision/blob/master/Images/led.png)
If the tensorflow support for python 3.5 and 3.6 is released please feel free to raise an issue.

### Demo:

