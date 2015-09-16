## Description ##

This Dockerfile is designed to work with dockerIDSEngines available at https://bitbucket.org/decodedtechsolutions/dockeridsengines
It also functions as a standalone instance.  Feel free to `docker run -it decodedtechsolutions/docker-snort-2.9.6.0 /bin/bash`  
If running as a stand alone instance, there are no rules or configuration provided.  

This installs snort 2.9.6.0 and some specific version of snort dependencies 

*	Ubuntu 12.04
*	snort 2.9.6.0
*	daq 2.0.2
*	libdnet 1.12
*	libpcap 1.5.3
*	pcre 8.34
*	zlib 1.2.8