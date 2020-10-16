## `openjdk:16-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6594ff13ca4fc911ebebc3f0a2c33242d9d642ed9fd34d802d80ecfacffc21e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:16-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:52361d81ab386337c3a59eb5439af5747dbe70efe7e687d7122a0c1ef531fa94
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297157752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f928eb3ec93c9819fcd51d76877c2d516c85aaeadf9f2893dba396d5b292b279`
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
# Fri, 16 Oct 2020 20:20:17 GMT
ENV JAVA_VERSION=16-ea+20
# Fri, 16 Oct 2020 20:20:58 GMT
COPY dir:bc2e1e657b5c0d6d4cc6bc79c6ea22e3d6ec7f8171568aba8ab12f7e004820ae in C:\openjdk-16 
# Fri, 16 Oct 2020 20:21:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 16 Oct 2020 20:21:28 GMT
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
	-	`sha256:81cc19cceaeceaab7b90201345588cbda919c6a7fdbe023204c37f8af1291feb`  
		Last Modified: Fri, 16 Oct 2020 20:31:19 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a157993b0071a842272353f38d81a53ab5c0cc3ffa3f3a8a95a8096741dd5c3a`  
		Last Modified: Fri, 16 Oct 2020 20:31:40 GMT  
		Size: 192.3 MB (192328282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c342a55a205b8c1221df5cd38136cefeb11fb6bdc57460ae4283c2c46cb8b662`  
		Last Modified: Fri, 16 Oct 2020 20:31:22 GMT  
		Size: 3.5 MB (3546753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2bd50abbd2e37136bf9d78fc7a6d0cd0d1d9d2a2d4670dbe18a5efb44c6e16`  
		Last Modified: Fri, 16 Oct 2020 20:31:19 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
