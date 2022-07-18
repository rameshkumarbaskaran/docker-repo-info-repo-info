## `openjdk:19-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:c0837734691a95b6c39c2eb9318d3a9e9daa2d707d0dcf3f29168ead63474aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:19-ea-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:b9d90466389a159b53cadb8f8b4d97fb294011d4df053e0aebde55264e80d0e1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298145479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cf5d31bad6ffb7158e254a63ca0218d8c2e5b0a09de8cd185023ce01530aa4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Wed, 13 Jul 2022 15:57:38 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 13 Jul 2022 15:57:39 GMT
USER ContainerAdministrator
# Wed, 13 Jul 2022 15:57:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Jul 2022 15:57:47 GMT
USER ContainerUser
# Mon, 18 Jul 2022 19:31:13 GMT
ENV JAVA_VERSION=19-ea+31
# Mon, 18 Jul 2022 19:31:28 GMT
COPY dir:e5d6c02cda6c9aad8297ef8b60a96b634aac97fc06764e8a0321aae4280bc02e in C:\openjdk-19 
# Mon, 18 Jul 2022 19:31:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 18 Jul 2022 19:31:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24a8dc780930fe59a9967fb76b10b2fb2ac36ff76c3697586a3df823f25ab8d`  
		Last Modified: Mon, 18 Jul 2022 21:24:44 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1582b9bf63a2d6ede0a45ecb506c093cf9a09b81e8de25dd46c5bffa9c7d94`  
		Last Modified: Mon, 18 Jul 2022 21:24:43 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4239363179c317c462b5006da97ce6faa8c7e4256719a99f4c3dd0cb7a4b524f`  
		Last Modified: Mon, 18 Jul 2022 21:24:43 GMT  
		Size: 69.0 KB (69030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262dd52e79d9b5ebce7877fd3f3e42eb3c3cfae509d375aa166c3a01cb8e29a9`  
		Last Modified: Mon, 18 Jul 2022 21:24:41 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa21cc7d85e5bb652e0a745be0edab2c61e1eb2afa60870ff6fe7c0ef6ebd8c9`  
		Last Modified: Mon, 18 Jul 2022 21:24:41 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af12c0f8b9fb58c6b7c7ced1abfd911438b4eacb8a10a8c6e3e2a4576527674`  
		Last Modified: Mon, 18 Jul 2022 21:25:02 GMT  
		Size: 191.2 MB (191199576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4020c73bfa16088d74c5847a68a20f000c3eafb2b03506b1ae05a743d93efc`  
		Last Modified: Mon, 18 Jul 2022 21:24:42 GMT  
		Size: 3.7 MB (3715243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd76fe5cba02d8d3a7728d15ce716140efddece6419b6cd3d7c52a2020d0ea2`  
		Last Modified: Mon, 18 Jul 2022 21:24:41 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
