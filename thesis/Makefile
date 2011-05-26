#Default all target just so that's what gets called when you just call "make"
all:

Makefile: ;

#Run with no target to build the thesis as a whole
clean:
	cd build && make clean
	rm -rf build
.PHONY: clean

build_dir:
	mkdir -p build
.PHONY: build_dir

#Forward all the other stuff to the one inside that cmake directory
%: force build_dir
	cd build && cmake ..
	cd build && make $@

force: ;
