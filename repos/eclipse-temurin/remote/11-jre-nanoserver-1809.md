## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b774889df73f8e2656bff9d34ea01b9d6f5b288b5006d55b935eb2f205ef5d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull eclipse-temurin@sha256:6a94bc327214fe99e23fa54af6c8bed11fb3a9c346de11fca4acfb4077ed62d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (146017610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96640f0e469bb1f75a2323d25dde893503a517315fdbbfda0c7518bd5c685135`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Thu, 10 Feb 2022 20:22:15 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Thu, 10 Feb 2022 20:22:16 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 10 Feb 2022 20:22:17 GMT
USER ContainerAdministrator
# Thu, 10 Feb 2022 20:22:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Feb 2022 20:22:33 GMT
USER ContainerUser
# Thu, 10 Feb 2022 20:27:50 GMT
COPY dir:7b430082d92796c7933d8991df8414f6ea317b19767304be325fe29c5d7cc52a in C:\openjdk-11 
# Thu, 10 Feb 2022 20:27:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5a7f567e84a5a148036156650a47ef7eec0187f17e880d3b475e51dacd70077b`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c012d3b7f4557f22093e79e3988a22ed074a31eb5a9365647e44ee6abb5c43`  
		Last Modified: Thu, 10 Feb 2022 20:47:07 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1310312626f8bd7ad3f88c405eb55492284f16f14ecadea3be9616cacfef6c50`  
		Last Modified: Thu, 10 Feb 2022 20:47:07 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8421e619570fefcfd211fe9d728dedd4e70946e12ba20f3c6580883a836da58`  
		Last Modified: Thu, 10 Feb 2022 20:47:06 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f951f36128cdb26f17d0d4a57c001ef78a30351c1d234786fd7906dc69a2efb0`  
		Last Modified: Thu, 10 Feb 2022 20:47:04 GMT  
		Size: 77.9 KB (77875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0055079e92dbe578c563d705dccb78ac46e37b520edb42b96df7f54a35d23f1b`  
		Last Modified: Thu, 10 Feb 2022 20:47:04 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32074591d51d54ed87614e6aac00aba603f95937c8db70e536154f9f722d8d3c`  
		Last Modified: Thu, 10 Feb 2022 20:49:27 GMT  
		Size: 42.8 MB (42758008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb02fd2c6e1adb2987f7be990457f58902354b04f5c9dbecbdccae1c566e7e0`  
		Last Modified: Thu, 10 Feb 2022 20:49:20 GMT  
		Size: 88.9 KB (88919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
