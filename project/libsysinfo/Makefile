MODULES=sysInfo cpuInfo pciInfo usbInfo
SOURCES=$(MODULES:=.cc)
HEADERS=$(MODULES:%=../%.h)

#  Location of openjdk headers.  Change this according to your 
#  version and architecture
OPENJDK=~/.jdks/openjdk-22.0.2/include

libsysinfo.so: $(SOURCES) $(HEADERS)
	gcc -fPIC -I .. -I $(OPENJDK) \
        -I $(OPENJDK)/linux -shared \
        -o libsysinfo.so $(SOURCES) -lstdc++

