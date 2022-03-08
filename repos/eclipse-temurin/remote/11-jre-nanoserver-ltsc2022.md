## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e94acb37e6a78ed1e8ebd1a74103ff36f7419fcd22bdf3830b2617082aa3719d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull eclipse-temurin@sha256:cd52be2caa56272ead12d7e7d31a091b6d55aaeb3c95119951689852ace165f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160398095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429031ca8bc20bba5103387cfeb3a24d68c4e50dd74cb937530523220733ece2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Tue, 08 Mar 2022 22:28:39 GMT
COPY dir:7b430082d92796c7933d8991df8414f6ea317b19767304be325fe29c5d7cc52a in C:\openjdk-11 
# Tue, 08 Mar 2022 22:29:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:021207e28f7e79ebf5daf05b42e671be1b646c30089a56e3a36eb9c78a7e4f71`  
		Last Modified: Tue, 08 Mar 2022 23:03:08 GMT  
		Size: 42.8 MB (42761992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676f76ce7fefa94e6963f93247f30d093f8b3d294d86e0ec3b29c2790b1039d5`  
		Last Modified: Tue, 08 Mar 2022 23:03:00 GMT  
		Size: 61.9 KB (61857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
