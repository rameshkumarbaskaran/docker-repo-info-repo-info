## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:52688d201e11b165fb6cdf435e373f83fb73da063a3673ec553b41cf94b7fbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull eclipse-temurin@sha256:62ce0548d5f27d9b34a53b599c0167d1773fb411c9f56d63e171b4a331fcbcf2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295312741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59e442e5a5ac9b273eb196d4d3f92c940f854b05fd8a1c221b5d78aa8a8f001`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Tue, 08 Mar 2022 22:06:10 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 08 Mar 2022 22:06:11 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 08 Mar 2022 22:06:12 GMT
USER ContainerAdministrator
# Tue, 08 Mar 2022 22:06:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Mar 2022 22:06:27 GMT
USER ContainerUser
# Tue, 08 Mar 2022 22:06:41 GMT
COPY dir:9ebff3631ec53abdcb6e4f307c52be82361e65c94c68bdde1fa726e2b087ad3f in C:\openjdk-11 
# Tue, 08 Mar 2022 22:06:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Mar 2022 22:07:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7898a841a8fb29f6e0fb4a59df2d203d086105d004a1ab238883a933abbe07`  
		Last Modified: Tue, 08 Mar 2022 22:42:06 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7956d3f3483f21113e3631e8aa2b7d5481e32730fa7fa771748c5695f16956ff`  
		Last Modified: Tue, 08 Mar 2022 22:42:06 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104ef6b7b424a4c884f4ddf49a14ab4b303c89e03483e5961cd617a0530505`  
		Last Modified: Tue, 08 Mar 2022 22:42:06 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58a025975ce316b76a358b0980cf7da83382e954630a16d78e77687e4159bff`  
		Last Modified: Tue, 08 Mar 2022 22:42:04 GMT  
		Size: 69.9 KB (69877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4256db85305558bcda525eeb76e811e0ea35c7a6559f62738066cb466100d608`  
		Last Modified: Tue, 08 Mar 2022 22:42:04 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00e2bf7525cf110084a50b4337b285017c60c86e699a0216fbed9e52d4e61a7`  
		Last Modified: Tue, 08 Mar 2022 22:45:50 GMT  
		Size: 192.1 MB (192087872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20e116266840c213a5eda44d45326c970171a4df9c2df47664f9b747aaf718b`  
		Last Modified: Tue, 08 Mar 2022 22:42:04 GMT  
		Size: 93.6 KB (93590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db53ae7b4ccc18026e80a36c69953ea34147e90ef923612317c79f7e06812586`  
		Last Modified: Tue, 08 Mar 2022 22:42:04 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
