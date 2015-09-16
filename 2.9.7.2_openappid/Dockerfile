FROM ubuntu:14.04
MAINTAINER Brandon Murphy <brandonr@DecodedTechSolutions.com>

# Install depends
RUN apt-get update && apt-get install -y --no-install-recommends \
	build-essential \
	bison \
	flex \
	libssl-dev \
	pkg-config \ 
	netbase

# Add source files
ADD src /usr/local/src/


# install specific version of major depends
RUN cd /usr/local/src/libdnet-1.12 && ./configure ; make ; make install
RUN cd /usr/local/src/libpcap-1.7.3 && ./configure ; make ; make install
RUN cd /usr/local/src/zlib-1.2.8 && ./configure ; make ; make install
RUN cd /usr/local/src/pcre-8.37 && ./configure --enable-jit --enable-pcregrep-libz --enable-pcre16 --enable-pcre32 --enable-utf --enable-unicode-properties ; make ; make install
RUN cd /usr/local/src/LuaJIT-2.0.3 && make ; make install

#Compile DAQ
RUN cd /usr/local/src/daq-2.0.4 && ./configure --disable-ipfw-module --disable-nfq-module --disable-ipq-module ; make ; make install

# Compile Snort
RUN cd /usr/local/src/snort-2.9.7.2 && ./configure --enable-control-socket --enable-sourcefire --enable-large-pcap --enable-zlib --enable-open-appid ; make ; make install

RUN ldconfig
RUN ln -s /usr/local/lib/libdnet.1.0.1 /usr/lib/libdnet.1
RUN mkdir /var/log/snort

RUN /usr/local/bin/snort -V


# CLEAN UP - TODO
