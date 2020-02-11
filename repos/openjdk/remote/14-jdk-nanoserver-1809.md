## `openjdk:14-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6dbf7f29c50c8313e14d01b12f9f4dd5e5eb9841d6e190ee9e50b94cc00a360c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:14-jdk-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:c547bf746ebf4be13428ed08ac7103296b91a7d303181d534f18194ee2578e42
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298538372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b5ef4a26174dca2deb0fe55a913542e854e32a5a9886f4e9f5d76382b39977`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2020 00:05:42 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 15 Jan 2020 00:05:43 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2020 00:05:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jan 2020 00:05:57 GMT
USER ContainerUser
# Tue, 11 Feb 2020 01:37:47 GMT
ENV JAVA_VERSION=14
# Tue, 11 Feb 2020 01:38:53 GMT
COPY dir:0d7510b7a9b226b4119fe9742b05f867c4806b739843cccbc6742c7969c1cdd8 in C:\openjdk-14 
# Tue, 11 Feb 2020 01:39:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Tue, 11 Feb 2020 01:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f3a5df9926db070e4016e42e49a7d9ce0131f528e644ae4388774831b6b46e`  
		Last Modified: Wed, 15 Jan 2020 01:58:21 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c21d67a14cad5558f706984eed7f97aaa2665e4b4cf1a7a1d21888c5e2c02a2`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ffd38236cfc5913ab84e035b74a0bddf197bbfffdd8e9e8b151cc30bbf8adb`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 66.5 KB (66486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8510d836b27dbac14cee7131c4209ebf2081c2ba957f75e05cbeff605e5320`  
		Last Modified: Wed, 15 Jan 2020 01:58:18 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85472e096d6bda035a58c2f6256a8d18bdf7e464065f2ed1bbf405670a504d9`  
		Last Modified: Tue, 11 Feb 2020 01:49:05 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4381dbab65cbdaa127181e737da29a3d6730dc43da7b43075505a1c4642e63aa`  
		Last Modified: Tue, 11 Feb 2020 01:49:27 GMT  
		Size: 194.0 MB (193965433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a8e6ff5e59842cf385c62e84dcd975376add04b1abddf1ac0a601913f91713`  
		Last Modified: Tue, 11 Feb 2020 01:49:06 GMT  
		Size: 3.4 MB (3446536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffd2776dbe34b58d6ed6f7bfc35ee2e46388f2cb7302f79dd2626f915a41c27`  
		Last Modified: Tue, 11 Feb 2020 01:49:05 GMT  
		Size: 915.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
