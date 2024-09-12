# nlte
Scripts to reproduce the calculations in Osorio et al. 2022 https://ui.adsabs.harvard.edu/abs/2022ApJ...928..173O/abstract

All scripts created Yeisson Osorio.

Required files to reproduce the synthetic spectra of
 k5888_4.1.METALS_-3.3C_1.0O_1.0N_1.0
 k6180_3.7.METALS_-5.6C_4.0O_3.0N_4.0
 k6390_4.4.METALS_-3.2C_1.0O_1.0N_1.0
in LTE and NLTE-m (Ca & Mg)

See paper for details. 

***** REQUIREMENTS *******
gfortran
python3
synple (https://github.com/callendeprieto/synple)


**** setup the files / codes *****
* goto tl208sy57

cd tl208sy54

*** REMEMBER change the flags in the Makefile to match your machine

make

* Done! all that is remaining is

*** test ***

cd ..

./runtest


