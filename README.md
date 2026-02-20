# ESP32-S3 Hello World

Prerequisites:

    sudo apt-get install git wget flex bison gperf python3 python3-pip python3-venv cmake ninja-build ccache libffi-dev libssl-dev dfu-util libusb-1.0-0

Install the development environment:

    mkdir -p ~/esp
    cd ~/esp
    git clone -b v5.5.3 --recursive https://github.com/espressif/esp-idf.git

After the download are completed:

    cd ~/esp/esp-idf
    ./install.sh esp32,esp32s3

Created the new project like this:

    idf.py create-project -p hello-esp32 hello-esp32

Needed to enter development environment:

    . ~/esp/esp-idf/export.sh

Configure project:

    idf.py set-target esp32s3
    idf.py menuconfig

Build:

    idf.py build

Flash:

    idf.py -p /dev/ttyACM2 flash monitor

USB-C cable connected to the "COM" connector (right) on the ESP32-S3 board. This
also displays the console output once the program is running.
