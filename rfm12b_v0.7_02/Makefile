CC=gcc
CFLAGS=-Wall
CFLAGSNOLINK=$(CFLAGS) -c 
LIBS= -lrt -lbcm2835
INC= -I/usr/local/include -I.

all: rfm12b_receiver

rfm12b_receiver: receiver.o rfm12b.o
	$(CC) $(CFLAGS) -o rfm12b_receiver receiver.o rfm12b.o $(LIBS) 

receiver.o: receiver.c
	$(CC) $(CFLAGSNOLINK) $(LIBS) -Wall receiver.c

rfm12b.o: rfm12b.c
	$(CC) $(CFLAGSNOLINK) $(LIBS) -Wall rfm12b.c
