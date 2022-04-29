## `openjdk:19-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:022f05944b4afe4102e3e573d3ff769cabbca2b339202d9bedd3bc89be65a680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `openjdk:19-jdk-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull openjdk@sha256:1569cce276075cedf24cdcbe02e6398b10ddbfce29667189975506ece20c9bf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296529400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8b1866cba9ae9e5bda9950fdd051b1c38e82140cbec42aafedc0dc0369bc81`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Wed, 13 Apr 2022 17:00:37 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 13 Apr 2022 17:00:38 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 17:00:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Apr 2022 17:00:44 GMT
USER ContainerUser
# Thu, 28 Apr 2022 23:19:49 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:20:04 GMT
COPY dir:ff1d04f640ce785192e5d827dc565eef22fd30c73bb78c2cf51fa31b13507a58 in C:\openjdk-19 
# Thu, 28 Apr 2022 23:20:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 28 Apr 2022 23:20:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4644baf69a04abfb80da969c1fb009552c461553f3672bd4e787c0ac7c37ea`  
		Last Modified: Tue, 19 Apr 2022 00:53:51 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61095df7d33e436b0d9cb0052f433e155a897f4278b9dc0a8d13582d6cad38ad`  
		Last Modified: Tue, 19 Apr 2022 00:53:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2110ca10faf88314f61157ce6bfeb157b8b8eebd74be6f0a78f2f7b82c514a`  
		Last Modified: Tue, 19 Apr 2022 00:53:51 GMT  
		Size: 68.8 KB (68813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d4716f16fd9ebec77b5cf5099ed25d889884b5a06da589ce896a7db47a15`  
		Last Modified: Tue, 19 Apr 2022 00:53:49 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a0e4220bdb68c84315e47b457412649165604b5f0ea9ac51353c78f7129e24`  
		Last Modified: Fri, 29 Apr 2022 04:28:42 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242cfc63fa61924f86b257366becd8f53e3aed3a96e834c75a8d1658094a91ad`  
		Last Modified: Fri, 29 Apr 2022 04:32:08 GMT  
		Size: 189.8 MB (189768864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4361256c76c20b38945d66745f484944f50598f28c879946cb241dd6624f0a`  
		Last Modified: Fri, 29 Apr 2022 04:28:46 GMT  
		Size: 3.6 MB (3588849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fc27a8a4fae13d18c3b30f40325c828aeaeaecfcb5c6f06173efba68021f8a`  
		Last Modified: Fri, 29 Apr 2022 04:28:42 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
