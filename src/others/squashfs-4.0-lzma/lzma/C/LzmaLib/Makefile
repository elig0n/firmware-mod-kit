CC = gcc
LIB = liblzma.a
RM = rm -f
CFLAGS = -c -O2 -Wall
AR = ar
RANLIB = ranlib

OBJS = \
  Alloc.o \
  LzFind.o \
  LzmaDec.o \
  LzmaEnc.o \
  LzmaLib.o \
  7zFile.o \
  7zStream.o \

all: $(LIB)

$(LIB): $(OBJS)
	rm -f $@
	$(AR) rcu $@ $(OBJS)
	$(RANLIB) $@

Alloc.o: ../Alloc.c
	$(CC) $(CFLAGS) ../Alloc.c

LzFind.o: ../LzFind.c
	$(CC) $(CFLAGS) ../LzFind.c

LzmaDec.o: ../LzmaDec.c
	$(CC) $(CFLAGS) ../LzmaDec.c

LzmaEnc.o: ../LzmaEnc.c
	$(CC) $(CFLAGS) ../LzmaEnc.c

LzmaLib.o: ../LzmaLib.c
	$(CC) $(CFLAGS) ../LzmaLib.c

7zFile.o: ../7zFile.c
	$(CC) $(CFLAGS) ../7zFile.c

7zStream.o: ../7zStream.c
	$(CC) $(CFLAGS) ../7zStream.c

clean:
	-$(RM) $(PROG) *.o *.a
