CC=gcc
CFLAGS=-I. -lsodium
DEPS=signcrypt_tbsbe.h
OBJ=test.o signcrypt_tbsbe.o

.PHONY: run-test

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

test: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS)

run-test: test
	./test

clean:
	rm -rf $(OBJ) test
