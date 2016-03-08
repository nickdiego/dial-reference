CC=$(TARGET)g++

.PHONY: clean
.DEFAULT_GOAL=dialclient

includes = $(wildcard *.h)
OBJS := main.cpp DialServer.cpp DialDiscovery.cpp DialConformance.cpp DialClientInput.cpp
CFLAGS=--sysroot=/home/nick/projects/iron-man/src/certi_hardware_diagnosis/.build_certi_desktop_linux_x86_64/prebuilt/host/usr/x86_64-buildroot-linux-gnu/sysroot/

# You may not need all these libraries.  This example uses a build of curl that needs crypto, ssl, cares, and zlib
dialclient: $(OBJS) ${includes}
	$(CC) -Wall -Werror -g $(OBJS) $(INCLUDES) $(CFLAGS) $(LDFLAGS) -ldl -lpthread -lcurl -lz -lcrypto -lssl -o dialclient

clean:
	rm -f *.o dialclient
