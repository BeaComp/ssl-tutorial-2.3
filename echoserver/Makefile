CC=gcc
CFLAGS=-Wall -I ../include
DEPS = ../include/unp.h
OBJ = echoserver.o

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

echoserver: ../lib/*.c tcpserv04.c
	$(CC) -Wall -o echoserver ../lib/*.c tcpserv04.c -I ../include -lm -lwolfssl

.PHONY: clean

clean:
	rm -f *.o echoserver
