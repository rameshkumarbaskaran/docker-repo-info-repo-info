## `openjdk:15-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:fc2718aa00385f2e10d6049c37524537f2b6ae51d40e71b2df2da866781ec592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:15-jdk-nanoserver-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:4bce0e7f3ce82b7e0a74075641cb0783705362edd9d47157c633ca30bc9a6d14
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298279282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f1890aa43c191ed0db3490bf075a983daf8644955713fdd4a9b245efc08cfe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 16 Feb 2020 01:25:57 GMT
RUN Apply image 1809-amd64
# Thu, 20 Feb 2020 02:05:49 GMT
SHELL [cmd /s /c]
# Thu, 20 Feb 2020 02:05:51 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 20 Feb 2020 02:05:53 GMT
USER ContainerAdministrator
# Thu, 20 Feb 2020 02:06:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 20 Feb 2020 02:06:21 GMT
USER ContainerUser
# Thu, 20 Feb 2020 02:06:23 GMT
ENV JAVA_VERSION=15-ea+10
# Thu, 20 Feb 2020 02:07:42 GMT
COPY dir:9e7f82d9e26ea20676a1fe5cca8e1806db85bd892784f6681c6fef79cc99c3d6 in C:\openjdk-15 
# Thu, 20 Feb 2020 02:08:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 20 Feb 2020 02:08:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a35da61c356213336e646756218539950461ff2bf096badf307a23add6e70053`  
		Size: 101.1 MB (101145811 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:141e7d00d8743fe3d0c951c1f46529a11bff09056f891a37a603bbde2491228e`  
		Last Modified: Thu, 20 Feb 2020 03:06:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e7d5fabfd691f6f12b0f526dd517b21dba9a0d86160f5a031a9915b3cebbe`  
		Last Modified: Thu, 20 Feb 2020 03:06:22 GMT  
		Size: 915.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797ce79628a34cd492d0a7deb2d4a028a4732ed656ba28675127d0d8ee1c7976`  
		Last Modified: Thu, 20 Feb 2020 03:06:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83840f341da670f768c8e90bfab9ea570671d70d0aedcf3fc430325628c790b7`  
		Last Modified: Thu, 20 Feb 2020 03:06:22 GMT  
		Size: 73.1 KB (73055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60136e35e1da9de137c41ef1a897b216fce1e005981f3ad3191275b74f94de9c`  
		Last Modified: Thu, 20 Feb 2020 03:06:19 GMT  
		Size: 928.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205685487b649f44767678c3dcecc24fd130659ef7e1ac461a6acb2cbb3f36f`  
		Last Modified: Thu, 20 Feb 2020 03:06:19 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c15bd03b9deaeb86895ab56c35ae88f1a645e14167d7e8152857dc9e8a7011e`  
		Last Modified: Thu, 20 Feb 2020 03:06:42 GMT  
		Size: 193.6 MB (193600258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e6e0884ea1c16472684741e1ca67a97bc7766c2d8e5278f67626d01e6dc6e3`  
		Last Modified: Thu, 20 Feb 2020 03:06:21 GMT  
		Size: 3.5 MB (3454583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba8d0939cb2cf71f3744ebc5a25f81d3c83a1aa3571dd92cf694d825e2f03fb`  
		Last Modified: Thu, 20 Feb 2020 03:06:19 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
