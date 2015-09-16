## Description ##

This Dockerfile is designed to work with dockerIDSEngines available at https://bitbucket.org/decodedtechsolutions/dockeridsengines
It also functions as a standalone instance.  Feel free to `docker run -it decodedtechsolutions/docker-snort-2.9.7.2_openappid /bin/bash`  
If running as a stand alone instance, there are no rules or configuration provided.  

This installs snort 2.9.7.2 and some specific version of snort dependencies 

*	Ubuntu 14.04
*	snort 2.9.7.2
*	daq 2.0.4
*	libdnet 1.12
*	libpcap 1.7.3
*	pcre 8.37
*	zlib 1.2.8
*	LuaJIT-2.0.3
