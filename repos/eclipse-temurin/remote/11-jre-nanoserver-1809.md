## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:cb94395b80882e9efa4c31ec23c1b564ba5876117ad7263576dc1a029d337949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull eclipse-temurin@sha256:3b19b8733ec4c2d10f396557edd32c5208f48da9c5c18a2ac824855895a33770
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145970528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922392a96d4a264194192abd0980e1f650c15dd1d358a1ad3f2f585f9ef53eeb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Tue, 08 Mar 2022 22:06:10 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 08 Mar 2022 22:06:11 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 08 Mar 2022 22:06:12 GMT
USER ContainerAdministrator
# Tue, 08 Mar 2022 22:06:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Mar 2022 22:06:27 GMT
USER ContainerUser
# Tue, 08 Mar 2022 22:11:00 GMT
COPY dir:7b430082d92796c7933d8991df8414f6ea317b19767304be325fe29c5d7cc52a in C:\openjdk-11 
# Tue, 08 Mar 2022 22:11:18 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7898a841a8fb29f6e0fb4a59df2d203d086105d004a1ab238883a933abbe07`  
		Last Modified: Tue, 08 Mar 2022 22:42:06 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7956d3f3483f21113e3631e8aa2b7d5481e32730fa7fa771748c5695f16956ff`  
		Last Modified: Tue, 08 Mar 2022 22:42:06 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7104ef6b7b424a4c884f4ddf49a14ab4b303c89e03483e5961cd617a0530505`  
		Last Modified: Tue, 08 Mar 2022 22:42:06 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58a025975ce316b76a358b0980cf7da83382e954630a16d78e77687e4159bff`  
		Last Modified: Tue, 08 Mar 2022 22:42:04 GMT  
		Size: 69.9 KB (69877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4256db85305558bcda525eeb76e811e0ea35c7a6559f62738066cb466100d608`  
		Last Modified: Tue, 08 Mar 2022 22:42:04 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d588ef95a7dec305481be2a379132794548bcbf27f4896e3dfa6b7e856a665`  
		Last Modified: Tue, 08 Mar 2022 22:46:56 GMT  
		Size: 42.8 MB (42758088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1bbb6f384bbeb939ff66b0168115e3167b7e8c8804294c35e8d8d4c79d962c`  
		Last Modified: Tue, 08 Mar 2022 22:46:47 GMT  
		Size: 82.3 KB (82258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
