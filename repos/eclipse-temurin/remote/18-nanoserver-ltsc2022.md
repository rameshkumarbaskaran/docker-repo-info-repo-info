## `eclipse-temurin:18-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ebe48c6baf54f9a56b9b27dda0ada345a24b5e57439009071aa1b5a3e21e2a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.768; amd64

### `eclipse-temurin:18-nanoserver-ltsc2022` - windows version 10.0.20348.768; amd64

```console
$ docker pull eclipse-temurin@sha256:50fe0080db6dae9db9f3abf91d02cb0fe4496aa6a2ec64827ce7bfdff11fe0b1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304544365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed092b4fa6ed6e7b71676556c6cababe8177cfff799c1bec50c8f63f58a9e34`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 18:08:52 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 18:13:52 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 15 Jun 2022 18:13:53 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 15 Jun 2022 18:13:54 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 18:14:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 18:14:05 GMT
USER ContainerUser
# Wed, 15 Jun 2022 18:14:22 GMT
COPY dir:dd9b13d03f0f59427148f5f854823680c639cd938d50ff4813e6410f92c7aca7 in C:\openjdk-18 
# Wed, 15 Jun 2022 18:14:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jun 2022 18:14:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:60cbdb7704dc53714205f32082d3faa20d7c93a53c40cb88f22581e85a2943fc`  
		Last Modified: Wed, 15 Jun 2022 19:13:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548edeb10e4bb743b69a9247eed1cce7535c1cf72730d3ad79120c94e4777af4`  
		Last Modified: Wed, 15 Jun 2022 19:22:52 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d433d0eb951a50620fd143ccc37bfdee174e986a9667e2130789f0cea31824`  
		Last Modified: Wed, 15 Jun 2022 19:22:52 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e674ac3369adee1947884c0a268657aaa682ee77094c2ab264a604a93f7ca116`  
		Last Modified: Wed, 15 Jun 2022 19:22:51 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0841f30e442afc7a145a17cd5534f47f77e30ed913efcb8c8d419a7dbb5c6509`  
		Last Modified: Wed, 15 Jun 2022 19:22:49 GMT  
		Size: 79.5 KB (79490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff48e0c8f74b8af8a996e4350347e31b641d89706e0a9e63e1ca85ddc68d6d7`  
		Last Modified: Wed, 15 Jun 2022 19:22:49 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe88a34cff6ef556307e1729646ae1edcd5a78d82130cc79e15a0fce87d7ec7`  
		Last Modified: Wed, 15 Jun 2022 19:26:14 GMT  
		Size: 186.4 MB (186421090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd4204bd98c62c226f91ddb1af5ae70dc7b413fb4d252e2a7fa8e4a505400d5`  
		Last Modified: Wed, 15 Jun 2022 19:22:49 GMT  
		Size: 60.8 KB (60799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9869b21dcdf1ff43fa93583f02824eb4eb012c5d0b231ae7d04a3da6a11b2462`  
		Last Modified: Wed, 15 Jun 2022 19:22:49 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
