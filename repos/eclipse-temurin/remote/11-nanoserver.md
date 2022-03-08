## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:79a55945efcc6884c01c46c735174e483ff675ae235104f5d1ec8d55111b58e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.587; amd64

```console
$ docker pull eclipse-temurin@sha256:da68e8609de315549362f501d245be4a2a75fcec9299a1c51bdd03e6746c1ec6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309738894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c9ce3479366bf28caf7084d8a69e00e54efe523372db1d2ec501389db82c5b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 04:50:34 GMT
RUN Apply image ltsc2022-amd64
# Tue, 08 Mar 2022 22:26:00 GMT
SHELL [cmd /s /c]
# Tue, 08 Mar 2022 22:27:29 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 08 Mar 2022 22:27:30 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 08 Mar 2022 22:27:31 GMT
USER ContainerAdministrator
# Tue, 08 Mar 2022 22:27:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Mar 2022 22:27:46 GMT
USER ContainerUser
# Tue, 08 Mar 2022 22:28:01 GMT
COPY dir:9ebff3631ec53abdcb6e4f307c52be82361e65c94c68bdde1fa726e2b087ad3f in C:\openjdk-11 
# Tue, 08 Mar 2022 22:28:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Mar 2022 22:28:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dad81795ce109a7e20ebf80ad31925797ed97f9ba2a559f13f96ce3be5ea712b`  
		Size: 117.5 MB (117485491 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ad17ae3a2fc5cdf554f0d828bd6d04e79f37ae3dd800a44c8a3a1892a57b75c3`  
		Last Modified: Tue, 08 Mar 2022 22:57:38 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389ae8041300b2fbe886df34a877508dec8bffd5facd02c7ecba5913c3d62030`  
		Last Modified: Tue, 08 Mar 2022 22:59:03 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea8ff3fdcc66a0c05495b8952b364730985bc4009dadd229495e84b90d11c99`  
		Last Modified: Tue, 08 Mar 2022 22:59:03 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfbc4003ad986d9e2cc35a68328e7a1feec0f0b9e0c14ead3000f2c3ffa1bbb`  
		Last Modified: Tue, 08 Mar 2022 22:59:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39143e9b465f180a64698fb5dd905716d2aed05ad72341f195db4d55834a15e`  
		Last Modified: Tue, 08 Mar 2022 22:59:00 GMT  
		Size: 83.0 KB (82965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80abffb98d53d204ae05b423789c0869800de2ce4e976eccc9dddf2df45814c3`  
		Last Modified: Tue, 08 Mar 2022 22:59:00 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d03525ebd00e7cbda979577dfb550739b952725ca66f11fe3b6ce1baffa2b8`  
		Last Modified: Tue, 08 Mar 2022 23:02:45 GMT  
		Size: 192.1 MB (192084997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4b7f5a365c059491b2984bcfca1d410c9ef3c62ef3a56f8601b306bb9b4318`  
		Last Modified: Tue, 08 Mar 2022 22:59:00 GMT  
		Size: 78.5 KB (78525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a200012ae70b88f53671e749d2b504abc13a338a75d2e451fd661c30a238e6a`  
		Last Modified: Tue, 08 Mar 2022 22:59:00 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.2686; amd64

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
