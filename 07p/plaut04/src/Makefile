.SUFFIXES:
.SUFFIXES: .c++ .o

OBJS = bifurcation.o solution.o stringtrim.o \
        tube.o polygon3d.o readFM.o createBoundingBox.o\
        createCoords.o axis.o createLegend.o gmain.o  \
        rounding.o printToPS.o createSphere.o createDisk.o \
        r3b/createLibPoint.o r3b/createPrimary.o r3b/gmainr3b.o \
        r3b/toInertialFrame.o

CXX=g++
INC=../../plaut04/includes
INCLUDES=-I$(INC) 
CFLAGS= -g -O2  -I/usr/X11/include
DEPS_LIBS=
MOC=
LIBS=$(DEPS_LIBS)

.c++.o:
	$(CXX) $(INCLUDES) $(CFLAGS) -c $< -o $@

../../bin/plaut04: $(OBJS)
	$(CXX) $(CFLAGS) -o $@ $(OBJS) $(LIBS)

gmainqt.moc.c++: gmainqt.h
	$(MOC) $< -o $@

clean:
	rm -f *.o gmainqt.moc.c++

axis.o: $(INC)/gplaut04.h axis.h
bifurcation.o: bifurcation.h createCoords.h rounding.h tube.h $(INC)/gplaut04.h
createBoundingBox.o: createBoundingBox.h
createCoords.o: createCoords.h $(INC)/gplaut04.h axis.h
createDisk.o: createDisk.h
createLegend.o: createLegend.h
createSphere.o: createSphere.h
gmain.o: $(INC)/gplaut04.h $(INC)/gVarNames.h bifurcation.h solution.h \
 createDisk.h createSphere.h createLegend.h readFM.h stringtrim.h
r3b/gmainr3b.o: $(INC)/gplaut04.h
gmainxt.o: solution.h bifurcation.h $(INC)/gplaut04.h
gmainqt.o: solution.h bifurcation.h $(INC)/gplaut04.h
printToPS.o: printToPS.h
polygon3d.o: polygon3d.h
readFM.o: readFM.h $(INC)/gplaut04.h
rounding.o: rounding.h
solution.o: solution.h createCoords.h rounding.h tube.h $(INC)/gplaut04.h
stringtrim.o: stringtrim.h
r3b/toInertialFrame.o: $(INC)/gplaut04.h
tube.o: tube.h polygon3d.h
