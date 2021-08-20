CC=nasm
FLAGS=-felf64
SRC := $(wildcard *.asm)
OBJ := $(SRC:.asm=.o)

%.o: %.asm
	$(CC) $(FLAGS) $< -o $@ 

triangle: $(OBJ)
	ld $^ -o $@ 

clean:
	rm -rf *.o triangle