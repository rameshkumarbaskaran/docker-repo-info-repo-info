## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c0e0e3a7bef9d3e1f0cd341710a68778722a20c8d661a99e26da041a907c66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.288; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:d1b2f24d7063b0d1b82853b09e3dfbd8add1a1599d90855ebb03a3525c36fe26
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156167755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e65899b0153f931ee4f9f09c860a20aecfa9e268b9c7062c4b087b66ea17da6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Wed, 13 Oct 2021 19:02:31 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 13 Oct 2021 19:02:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Oct 2021 19:02:32 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 19:02:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Oct 2021 19:02:49 GMT
USER ContainerUser
# Wed, 13 Oct 2021 19:03:28 GMT
COPY dir:1080d1f1dd1c0d61d0c45958055fb50fcd7599d7396f8e079867cfa7dbefbee8 in C:\openjdk-8 
# Wed, 13 Oct 2021 19:03:42 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b013d8b98acd715c3c13d7de9f98d64676bf2486d547545d93a56a2c576fa73`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a42ef6fca9ff05407154bf2b7a418a8bd467bfc933bc6581b4047ab17275b46`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89143e1acad2a5116c8dbf4a95f6b172d88a5a7eaa294a77716905013b158cff`  
		Last Modified: Wed, 13 Oct 2021 19:43:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445a48e48b51c51d06acc0d3d461be030307abf6f59a157ec3de316f1c5261f8`  
		Last Modified: Wed, 13 Oct 2021 19:43:52 GMT  
		Size: 85.8 KB (85779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38acab5055fb1449f4474f91c3cd41b4b22cdbf33ef43143b6e269512e2f85a`  
		Last Modified: Wed, 13 Oct 2021 19:43:52 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d015cefbbd055b87228eb1f8160b28752fb6f463511920f8e4daeafe96136bf`  
		Last Modified: Wed, 13 Oct 2021 19:44:58 GMT  
		Size: 39.1 MB (39074857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998490882e1871bdf58453765ed6f272791fc42c4d418b5c9f958315ce863561`  
		Last Modified: Wed, 13 Oct 2021 19:44:15 GMT  
		Size: 61.8 KB (61813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
