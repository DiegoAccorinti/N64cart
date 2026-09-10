# N64cart

<img width="428" height="500" alt="imagen" src="https://github.com/user-attachments/assets/bb808214-e0ff-484d-9d0b-aa795c0dd05f" />

archivos necesarios para el cartucho chino N64 basado en PICO (no es PICOcart64)

compilar la herramienta:<br/>
sudo apt update<br/>
sudo apt install git build-essential libusb-1.0-0-dev<br/>
cd ~<br/>
git clone https://github.com/pdaxrom/N64cart.git<br/>
cd N64cart/utils<br/>
make<br/><br/>


1.  Flashear la PICO con el archivo n64cart.uf2
2.  verificar con $ lsusb  que aparezca:<br/>

Bus 001 Device 022: ID 1209:6800 Generic N64<br/>

3.  formatear la memoria con :  $ sudo ./usb-romfs format
4.  copiar el administrador de juegos:  $ sudo ./usb-romfs push n64cart-manager.z64
5.  copiar imagen de fondo:  $ sudo ./usb-romfs push n64.jpg
6.  copiar el resto de los juegos .z64
