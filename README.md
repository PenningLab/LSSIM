# DDM
Direct DM Pythia toy model

Code for platform independent development at the bottom, first the actualy code: 

## Setting up environment and compile

```bash
source init/init_geant4_plus_ROOT.sh
```

compile:

```bash
mkdir build
cd build
cmake -DGeant4_DIR=/cvmfs/geant4.cern.ch/geant4/10.2.p02/x86_64-slc6-gcc49-opt/lib64/  ../
make -j
```

Execute:
```bash
./DDlight
```



## Vagrant instructions

The code is based on CERN scientific linux. Vagrant allows to develop and execute platform independent. All dependencies and
instructions are enclosed in the single 'vagrantfile'. The machine has to have installed:

* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)

The Vagrant box in use is the CernVM.

NOTE: By default this setup will use 2 cores and 2 GB of RAM. To adjust these numbers edit the Vagrantfile before continuing. 

Perform the following steps:

1. Clone repository: ```git clone https://github.com/bpenning/DDlight DDlight```
2. Open terminal (or powershell on Windows)
3. Change into the project directory: ```cd DDlight```
4. Lastly execute and ssh into virtual machine:
```bash
vagrant up # can take a few min, particular at first start
vagrant ssh
cd /vagrant
```

Now follow the instructions above for initialising the development environment, compile and execute the code. Other useful commands after work is done is ```vagrant suspend``` and ```vagrand halt```.


== hello ==