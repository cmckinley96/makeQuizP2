# Colin McKinley
#Makefile for makequiz

all: build doc doczip

myexe: build

html: doc

index.html: doc

build: college.o collegemain.o course.o
	g++ -o myexe college.o collegemain.o course.o

college.o: college.cc college.h
	g++ -c college.cc

collegemain.o: collegemain.cc
	g++ -c collegemain.cc

course.o: course.cc course.h
	g++ -c course.cc

doc:
	doxygen -g
	doxygen Doxyfile

doczip:
	doxygen -g
	doxygen Doxyfile
	zip -r doczip.zip ./html

clean:
	rm *.o myexe
	rm Dox*
	rm -rf html latex
