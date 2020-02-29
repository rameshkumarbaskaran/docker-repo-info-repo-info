## `openjdk:15-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:39010bc88dca361c69089f3c4bb790cbfadfa84b55709021891c728a958b2fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:15-ea-nanoserver-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:a733d2fd7a3d32573ba6049298a0a42a422160237bb08cca6f0eeb538b901a1b
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297957693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560b13901617bea3536372c6042a8012738bfdadde2f17e2f67837317bb08fb6`
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
# Sat, 29 Feb 2020 01:39:40 GMT
ENV JAVA_VERSION=15-ea+12
# Sat, 29 Feb 2020 01:40:38 GMT
COPY dir:42ea89e58b2ba522bc89d358099a0b6125366596be92ce39382b015ecdb6efa5 in C:\openjdk-15 
# Sat, 29 Feb 2020 01:41:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Sat, 29 Feb 2020 01:41:04 GMT
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
	-	`sha256:766c9b36ec0a5061e22f701cb40ebc840b40f782db8e39b664329862bc803c3e`  
		Last Modified: Sat, 29 Feb 2020 01:48:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b316e29cd3ec0bacf5629b4eb2d894bb1d6d487dd39be5517629bcf4bbf89f`  
		Last Modified: Sat, 29 Feb 2020 01:49:17 GMT  
		Size: 193.3 MB (193297121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d658f4190b975e19e5c1bb64546ec5b27aa8346c92a09319754008075506c2cd`  
		Last Modified: Sat, 29 Feb 2020 01:48:56 GMT  
		Size: 3.4 MB (3436132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b07690ee24f736bc37a222e5fa69e68e405bf2f4f32eb403c3c78a25bf0e3a`  
		Last Modified: Sat, 29 Feb 2020 01:48:54 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
