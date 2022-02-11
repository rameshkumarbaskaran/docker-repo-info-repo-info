## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b0ab08e0e2b4de38bb2f3bc57fa38418738cc0a9d01d51387cdbac348874c858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull eclipse-temurin@sha256:c7a40c97282bd6354e012f231ff5a05adab1812040a7bb77b2ac0525a357d3ca
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302640221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f547d487acb7941e45888980675cd14a6878b0ef9bc5951bde9668046029792`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 01 Feb 2022 02:25:40 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Feb 2022 20:19:59 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 20:23:11 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Wed, 09 Feb 2022 20:23:12 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Feb 2022 20:23:13 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 20:23:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Feb 2022 20:23:23 GMT
USER ContainerUser
# Wed, 09 Feb 2022 20:23:56 GMT
COPY dir:af72ba1102e9cda7f5ea9974b0cafbe96b2f97690adb0743202a1c732a987a84 in C:\openjdk-17 
# Wed, 09 Feb 2022 20:24:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Feb 2022 20:24:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ab33c1d9cc1eaef56d5617b87373ead45d8a4ff7ab7da384afe612ba569a524`  
		Size: 117.5 MB (117457656 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3caa1e550ae326513f81130f539f06a05b30aca3f6ac96039cce37a715c5f008`  
		Last Modified: Thu, 10 Feb 2022 21:15:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c137f6d443ab391dba81e3ea945e6ef6f4b3abe558872170a36ce7d1491c369`  
		Last Modified: Thu, 10 Feb 2022 21:19:57 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2cc915fa9de18f231edb0d38aaec021a7704c97fea59e3924ae50ec434b423`  
		Last Modified: Thu, 10 Feb 2022 21:19:57 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1f04355408f8d28280a3e5e77355eb637128027fe3fe102eb9f1508aad7be1`  
		Last Modified: Thu, 10 Feb 2022 21:19:57 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e75318cd44ff95d4b5b1f45c1db4a0f9424efbbcda05b14b92ed4a295d0f86`  
		Last Modified: Thu, 10 Feb 2022 21:19:55 GMT  
		Size: 84.0 KB (83998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacd5585314d12d6a114a0baae148677958f857e374bb2a23fffd6a575ff726`  
		Last Modified: Thu, 10 Feb 2022 21:19:55 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2e5309d7a2daaa81d1e2a30ffe9cdf88b25b987a538e543d6a7b40b2ac9883`  
		Last Modified: Thu, 10 Feb 2022 21:23:06 GMT  
		Size: 185.0 MB (185028687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c72e928469926692944a37c4da71f6ba3a5d095e48fa511cb5e97a286cb540`  
		Last Modified: Thu, 10 Feb 2022 21:19:55 GMT  
		Size: 62.9 KB (62944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695a59eb35f3ead54fcdcff14b82e0b82651898d8c6fc1f9ce5a3917135ff2e0`  
		Last Modified: Thu, 10 Feb 2022 21:19:55 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
