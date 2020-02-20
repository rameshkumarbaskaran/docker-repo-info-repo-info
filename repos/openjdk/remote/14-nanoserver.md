## `openjdk:14-nanoserver`

```console
$ docker pull openjdk@sha256:22e3c3d6b2d5c38087580f7924dbceca188fd824883457574afa402391bf54fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:14-nanoserver` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:7e99f932a8b48bd8fcc9238d32ce9dd3a872fd4bebb0c0894cc0edc78532d5f4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298631829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c000e893fe575967697a6d2e35c8830f964796dcd31a012cfebec65cfc6df74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 16 Feb 2020 01:25:57 GMT
RUN Apply image 1809-amd64
# Thu, 20 Feb 2020 02:05:49 GMT
SHELL [cmd /s /c]
# Thu, 20 Feb 2020 02:24:49 GMT
ENV JAVA_HOME=C:\openjdk-14
# Thu, 20 Feb 2020 02:24:50 GMT
USER ContainerAdministrator
# Thu, 20 Feb 2020 02:25:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 20 Feb 2020 02:25:07 GMT
USER ContainerUser
# Thu, 20 Feb 2020 02:25:09 GMT
ENV JAVA_VERSION=14
# Thu, 20 Feb 2020 02:25:59 GMT
COPY dir:0d7510b7a9b226b4119fe9742b05f867c4806b739843cccbc6742c7969c1cdd8 in C:\openjdk-14 
# Thu, 20 Feb 2020 02:26:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 20 Feb 2020 02:26:22 GMT
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
	-	`sha256:b2c1f15a52f166cbc36848c52993d1c12e2e60320ca7065a723c5b9b75ae9d1b`  
		Last Modified: Thu, 20 Feb 2020 03:12:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fc58d70c7a7f37b34ca10b30dd6987cbd65bf702c1d343fca1bec1eb73f7c1`  
		Last Modified: Thu, 20 Feb 2020 03:12:27 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe218ee7b3e67683a6265541975293e853922aef1393a611015c5d7b5898c18c`  
		Last Modified: Thu, 20 Feb 2020 03:12:27 GMT  
		Size: 68.2 KB (68238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eaa90dc9c17da78b3f41b76dd90116d4e41e09c77988b4594ba5ba789c1e1f`  
		Last Modified: Thu, 20 Feb 2020 03:12:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84f48035843a5429ee2bbec02fa5eae051ca06d4f48c6fb23baf565e00b0511`  
		Last Modified: Thu, 20 Feb 2020 03:12:23 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98798c943089495f795a1d3115b0498abc96d178c58537ae7b2a81a97671cf4`  
		Last Modified: Thu, 20 Feb 2020 03:15:37 GMT  
		Size: 194.0 MB (193965657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9fbe563220d3fc5292d0ff9bbaa283aa9366f7c696cc027369df66b7960ab6`  
		Last Modified: Thu, 20 Feb 2020 03:12:24 GMT  
		Size: 3.4 MB (3446514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c61e571e05a99dc50158ec5f53387eb9928ddb73c59b13aefd8a2e3c80908b`  
		Last Modified: Thu, 20 Feb 2020 03:12:23 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
