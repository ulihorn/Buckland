include ../../config

all: glut_test

# if using fink on darwin
# you need these additional flags
CPPFLAGS = -I/sw/include -L/sw/lib

glut_test: glut_bind.cpp
	$(CXX) glut_bind.cpp -o glut_bind -I$(LUA_PATH)/include -I- -I$(BOOST_ROOT) $(CPPFLAGS) \
	-I../../ -I/usr/X11R6/include -L/usr/X11R6/lib -L$(LUA_PATH)/lib -L../../lib \
	-lluabind -lX11 -lXi -lXmu -lglut -lGL -lGLU -lm -llua -llualib

clean:
	rm -f glut_bind.o

