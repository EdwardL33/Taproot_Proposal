## CURRENT WAY TO FLASH ##

### INITAL SETUP ###
- go into main folder (Taproot_Proposal)
- ```cd template-project```
- ```pipenv install --python="3.9"``` (pipenv --rm (if you mess up))
- ```pipenv shell (type exit to leave pipenv)```

### REGENERATE TAPROOT TO ADD MODULES ###
(if you're in \template-project\ directory)
```
cd ..;                                        
rm -r template-project\taproot; 
cd .\template-project\;
lbuild build; 
scons build
```

### BUILDING AND FLASHING ###
- ```pipenv shell```
- ```scons build```
- ```openocd -f interface/stlink.cfg -f target/stm32f4x.cfg  -c "program ./build/hardware/scons-release/template-project.elf verify reset exit"```

## ADDING NEW BOARD ##
TODO
