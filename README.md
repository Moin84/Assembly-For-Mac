# How to run assembly code on mac silicon processor?

first install homebrew from https://brew.sh/
then install nasm using this command-

brew install nasm


now write your assembly code and if file name is file-name.asm, use these terminal commands to run-

nasm -f macho64 -o file-name.o file-name.asm
ld -o file-name file-name.o -lSystem -syslibroot $(xcrun --show-sdk-path) -e _start -platform_version macos 10.12 11.0
./file-name
