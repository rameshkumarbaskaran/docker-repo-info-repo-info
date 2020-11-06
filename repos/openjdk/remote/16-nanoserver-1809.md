## `openjdk:16-nanoserver-1809`

```console
$ docker pull openjdk@sha256:ed8d9786a577957e8c73a79162a5b229bd48de7e77f9dc8fb36d684284bb13c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:16-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:bd00d9509120b20878a59170eb541029518a62cad7cf45a5296273b108efd4d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283649824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c83f3993c717514c42b2ed858b1c1e8b04f2d071fd2fb082fc0ec9eeba7981c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 17:46:04 GMT
SHELL [cmd /s /c]
# Wed, 14 Oct 2020 17:46:05 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Oct 2020 17:46:06 GMT
USER ContainerAdministrator
# Wed, 14 Oct 2020 17:46:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 14 Oct 2020 17:46:22 GMT
USER ContainerUser
# Fri, 06 Nov 2020 18:20:29 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 06 Nov 2020 18:21:03 GMT
COPY dir:32805abd9af50dd1ad5b5a4bc83c7f61360fd8cc7b0d8a6e1fd0108cebd60472 in C:\openjdk-16 
# Fri, 06 Nov 2020 18:21:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 06 Nov 2020 18:21:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:40f59dc77cd194db29e444ce30cc9a91a3d555f7d4d7329fb6f46c13e559dc2f`  
		Last Modified: Wed, 14 Oct 2020 18:31:55 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2c5c7ff5b97e2384ad57c7cd4094b1a40907ea3634e923a539236764052c20`  
		Last Modified: Wed, 14 Oct 2020 18:31:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e535cf22ef1ca77aebd1948de6ab3937b1f63d64895ea717d71cff42d95815`  
		Last Modified: Wed, 14 Oct 2020 18:31:54 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a209bbfc514f45496baa96d8592838b00434aae4cd11fb8ffbcf643dfe386c`  
		Last Modified: Wed, 14 Oct 2020 18:31:52 GMT  
		Size: 72.2 KB (72249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc31a2a793752d0400745705f15ea0e51a67ed288dc5bc3c6eda4520ca139549`  
		Last Modified: Wed, 14 Oct 2020 18:31:50 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d7548fc9a07edf021119be39022a3c6d3db5dce4239373adfc3742224afc6c`  
		Last Modified: Fri, 06 Nov 2020 18:27:03 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf9ab0af7262c6f5ed1dd61f1c07e6bf7ccdba1053ee237ee580251ed57cd55`  
		Last Modified: Fri, 06 Nov 2020 18:27:20 GMT  
		Size: 178.7 MB (178726494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e580a90f0f13e10797801c907bb2cbb58e117abefb6bdf44daf03f18b20e7350`  
		Last Modified: Fri, 06 Nov 2020 18:27:07 GMT  
		Size: 3.6 MB (3640594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17f0b57020aefea072e1f2cde19580890ddd96de55b16d7af04ab829763f3f9`  
		Last Modified: Fri, 06 Nov 2020 18:27:02 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
