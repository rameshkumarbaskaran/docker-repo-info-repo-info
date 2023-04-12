## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2b785f1d4fedacc4800241fb73d501ee25434b1536ee2ca7213bd77b80601dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull eclipse-temurin@sha256:396a5e012895e08091fc127aaf3c0266cf546e1eafcbc083080f49a2fdbffb36
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165779272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a306ebe34964e0d56108160683d4977ea0b1d46e9c58ca5cac4909f1d5a774`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:16 GMT
RUN Apply image 10.0.20348.1668
# Wed, 12 Apr 2023 01:42:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Apr 2023 01:45:50 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Wed, 12 Apr 2023 01:45:51 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Apr 2023 01:45:51 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 01:46:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Apr 2023 01:46:03 GMT
USER ContainerUser
# Wed, 12 Apr 2023 01:47:01 GMT
COPY dir:bfcbd3aaadac52e2fbf5597edb59a69874950e88ce16232f7581c0ac600a935c in C:\openjdk-17 
# Wed, 12 Apr 2023 01:47:19 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:e06b772d586b58466a653b72002aee7c59496110e9ae402ff58f026e44452506`  
		Last Modified: Wed, 12 Apr 2023 02:34:14 GMT  
		Size: 122.3 MB (122328782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8058ec80ac2516d001291dea383d4abfa22416397a4c869e6fd79c0d4b64565f`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbccf86aba754c96fec3392364249e60424924cb4ecd3ef3fd1173fdf59dbd0a`  
		Last Modified: Wed, 12 Apr 2023 09:47:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a6af2e3b4b49b11dafa6baa7abb7124b85b7dffaada1e60410f3b182b5440d`  
		Last Modified: Wed, 12 Apr 2023 09:47:08 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23fbea9a6aad406b2f0d73eebd255c578b52cb3d992e90d1a490dcef510c127`  
		Last Modified: Wed, 12 Apr 2023 09:47:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0853e1de5f76cccd350c367db8bff4fcad9ca15d2bd1905bfdf6d9ff5bc745`  
		Last Modified: Wed, 12 Apr 2023 09:47:06 GMT  
		Size: 81.3 KB (81333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c1ec806b6b017a38be0ba594da25d03f5079eb81ca9e62a9dd176c6c78465b`  
		Last Modified: Wed, 12 Apr 2023 09:47:06 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33905fb21e1bfce4fae990c2149b381244ac5dfb9435e30d12468d13192a004`  
		Last Modified: Wed, 12 Apr 2023 09:47:47 GMT  
		Size: 43.3 MB (43301945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af01597888db384aa9f6a469bd9875ece40f625ac44ac4c0efdaf7db74a9ad79`  
		Last Modified: Wed, 12 Apr 2023 09:47:38 GMT  
		Size: 61.9 KB (61868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
