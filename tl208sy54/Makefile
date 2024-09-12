SH = /bin/bash
FC = gfortran
LINUXFLAGS = -fno-automatic -mcmodel=medium
MACFLAGS = -fno-automatic
FFLAGS = $(LINUXFLAGS)

all: down filesout tlsy

down: download
	$(SH) download 

filesout: 
	unzip data_atom.zip 
	unzip EMPSyo2021.zip
	unzip tlusty_synspec.zip
	cd tlusty_synspec ; unzip linelist.zip -d linelist

tlsy:  tlusty_synspec
	cd tlusty_synspec/synspec ; $(FC) $(FFLAGS) s54h.f -o synspec.exe 
	cd tlusty_synspec/tlusty ; $(FC) $(FFLAGS) tlusty207.f -o tlusty.exe 

clean:
	rm *.zip *.tar.gz
	rm -r tlusty_synspec
	rm -r linelist
	rm -r data_atom
	rm -r EMPSyo2021
