# Vivado Download Crawler
Python script to automate the process of downloading specific versions of Vivado/Vitis binaries from the AMD Xilinx website, without the need of a GUI. This script takes care of finding the specified version, signing in, filling necessary information and saving the files locally.

## Prerequisites
**This was tested on Ubuntu 20.04, using Python 3.10.5**

To setup the environment, first update your packages:
```bash
sudo apt-get update
sudo apt-get upgrade
```

Install Google Chrome:
```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt-get install -y ./google-chrome-stable_current_amd64.deb
```

Install the following packages, creating a virtual env is recommended:
```bash
pip install selenium webdriver-manager
```

## Usage
Once the prerequisites are installed, you can run the script to automatically download the specified version of Vivado binaries.

### Command-line Usage
Run the script from the terminal with the following options:
```python
python main.py -v <vivado_version> [-o <output_directory>, -t <timeout>]
```

### Example
```python
python main.py -v 2024.1 -o /home
```
This will download Vivado version 2024.1 and store the files in /home. If you do not specify an output directory, the script defaults to downloading the files to $HOME.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
