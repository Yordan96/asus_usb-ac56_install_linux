# asus_usb-ac56_install_linux
Instrucciones de instalación de Driver del dispositivo usb-ac56 para sistema operativo Linux

- 1. Se debe Clonar el repositorio 
```
sudo git clone https://github.com/gordboy/rtl8812au-5.9.3.2.git 
```
Espejo en mi repo
```
sudo git clone https://github.com/Yordan96/asus_usb-ac56_install_linux
```


- 2. instalar en el sistema dkms y build-essentials
```
sudo apt install git build-essential dkms
```

- 3. Instalar el driver
```
sudo cp -r rtl8812au-5.9.3.2 /usr/src/rtl8812au-5.9.3.2
sudo dkms add -m rtl8812au -v 5.9.3.2
sudo dkms build -m rtl8812au -v 5.9.3.2
sudo dkms install -m rtl8812au -v 5.9.3.2
sudo dkms status
```

Si se quiere desinstalar correr
```
sudo dkms remove -m rtl8812au -v 5.9.3.2 --all
```
