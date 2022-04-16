## Installing Ubuntu 20.04.04 Using Serial Console with speed 9600

* Edit isolinux.cfg add "SERIAL 0 9600"

* At Installation Menu, press "e" while Install Ubuntu Server is selected. Point the console to the corresponding tty by adding console=ttyS0,9600 text as a parameter of linux command. Remove quiet option. Example:
  ```
    set gfxpayload=text
    linux	/install/vmlinuz  file=/preseed/ubuntu-server.seed console=ttyS0,9600 text ---
    initrd	/install/initrd.gz
  ```

* Press CRTL + X on the keyboard to boot machine 

* The machine should boot using the Install Ubuntu option which is usually the first option in the menu

* After that you should be able to navigate the installation screen using the arrows keys
