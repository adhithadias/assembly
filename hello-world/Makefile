CC=nasm
FLAGS=-felf64
SRC := $(wildcard *.asm)
OBJ := $(SRC:.asm=.o)

%.o: %.asm
	$(CC) $(FLAGS) $< -o $@ 

hello: $(OBJ)
	ld $^ -o $@ 

clean:
	rm -rf *.o hello