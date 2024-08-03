First of all this is the repo that this config focuses on: 

https://github.com/petejohanson/zmk/blob/feat/pointers-move-scroll/app/include/dt-bindings/zmk/mouse.h

git clone -b feat/pointers-move-scroll https://github.com/petejohanson/zmk


or just clone this repo 

git clone -b move-scroll-pointer-working-version https://github.com/abastola0/zmk-config.git


-- copy the ./runthistobuild.sh inside app which is inside the zmk repo

-- setup native flashing as mentioned here: https://zmk.dev/docs/development/setup/native



1. first create a virtual env 
    conda create -n zmk python
2. activate the env
    conda activate zmk
3. install west
    pip install west
4. init app and update: note you need to be inside zmk
    west init -l app/
    west update
5. Makesure the zephyr is properly installed following the repo guidelines for native build
    west zephyr-export
6.  install zephyr scrips
    pip install -r zephyr/scripts/requirements-base.txt
7. then go inside the app inside zmk and do ./runthistobuild.sh








