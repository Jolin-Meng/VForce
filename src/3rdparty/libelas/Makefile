include ../../src/Makefile.conf

MODULE_NAME = LIBELAS
MODULE_COMMENT = Disparity Map

LINK = g++
CXXFLAGS += -w -msse3 -O3 -fopenmp
LFLAGS += -lipc -lglobal -fopenmp
 
SOURCES = descriptor.cpp elas.cpp filter.cpp main.cpp matrix.cpp triangle.cpp
TARGETS = libelas.a test

ifndef NO_PYTHON
TARGETS += libelas.so.1
endif

test: main.o libelas.a

libelas.a: descriptor.o elas.o filter.o matrix.o triangle.o

libelas.so.1: descriptor.o elas.o filter.o matrix.o triangle.o

clean: clean_libelas

clean_libelas:
	rm -rf *.o *.a *~
				 
# rules
include ../../src/Makefile.rules


