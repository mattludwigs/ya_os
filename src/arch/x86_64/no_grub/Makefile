arch ?= x86_64

clean:
	rm -r build

build: compile 
	mkdir -p build
	mv boot.bin build/

run: build
	qemu-system-$(arch) build/boot.bin

compile:
	nasm boot.asm -f bin -o boot.bin
