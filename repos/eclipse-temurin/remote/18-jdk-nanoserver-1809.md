## `eclipse-temurin:18-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:1c09b9d423c51c2326137bd3aec658deebb97d3b0d5d91d0aa31a9a2bf373118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `eclipse-temurin:18-jdk-nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull eclipse-temurin@sha256:96e08b25cc6fedd1a367298f29ad4645ae1e0a1624468fcb0059c08bebbd5fb8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293223791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbcd98a3aae95bdadd4152ee4255ee19cac0aa3a35f488d058cc8892c19c196`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 18:03:13 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 15 Jun 2022 18:03:14 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 15 Jun 2022 18:03:15 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 18:03:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 18:03:27 GMT
USER ContainerUser
# Wed, 15 Jun 2022 18:03:43 GMT
COPY dir:dd9b13d03f0f59427148f5f854823680c639cd938d50ff4813e6410f92c7aca7 in C:\openjdk-18 
# Wed, 15 Jun 2022 18:04:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jun 2022 18:04:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80401a436084179d205c8c414a595f0f5f88c6f2cef1f808b2adda75120906df`  
		Last Modified: Wed, 15 Jun 2022 19:06:19 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ac3cf2eeddadcc0472d451142ef88b9951fa1080e0d5c711d01745bbe23e6`  
		Last Modified: Wed, 15 Jun 2022 19:06:18 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01935e2bd054ecaeddc9a097fe94873beb8b15d2849846336f56930aa195192c`  
		Last Modified: Wed, 15 Jun 2022 19:06:19 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f37aed99aa70d21c9042c2ef0fe8d5701bc48b3168293f4204e6e09e9a6bfe`  
		Last Modified: Wed, 15 Jun 2022 19:06:16 GMT  
		Size: 70.3 KB (70272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7565f6e8337ca088f94791a3a73f31ee22bd7c73a97d845575f38b434c10cb`  
		Last Modified: Wed, 15 Jun 2022 19:06:16 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944d25c5e599229900dbe35ae40ac81b0c60387420a60901d4bd1ee02d903bf`  
		Last Modified: Wed, 15 Jun 2022 19:09:32 GMT  
		Size: 186.4 MB (186434750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab9237a624769d7ea377bac52189d81d9ee1a11990ee2813708b8174714b121`  
		Last Modified: Wed, 15 Jun 2022 19:06:20 GMT  
		Size: 3.6 MB (3558553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c499778fa45a52da38a68973bd804d9011f2e99bd13c72b65cd45d2356fbce9`  
		Last Modified: Wed, 15 Jun 2022 19:06:16 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
