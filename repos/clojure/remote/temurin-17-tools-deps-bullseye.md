## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:984e0512216debd4e20bf96c6e71f8494b735984f3b915d540e496e92e5aa213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ea2d502bdf436d7aeecb0186be9ed2e9d0558c4448147b69544822bd2743f4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319508564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaea529616886a13d7ce2c23dde86608bb0650813bce432442a9160fc1a3f181`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 08:09:51 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 08:09:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:11:41 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Tue, 23 May 2023 08:11:41 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:11:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 23 May 2023 08:11:57 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 May 2023 08:11:57 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 08:11:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 08:11:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62e3a1941399287928e0b128fbf9c001cd1f164f2cd9d5b0f242162cb22481`  
		Last Modified: Tue, 23 May 2023 08:18:28 GMT  
		Size: 192.6 MB (192580373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371c3883c04257bc7977ed94794c6a31958a8da76ec0a220ea4b3994e980baa5`  
		Last Modified: Tue, 23 May 2023 08:19:23 GMT  
		Size: 71.9 MB (71878148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba9281399e0eb61e935271010e815dd10b0e3b076a93c881469f4d58943e953`  
		Last Modified: Tue, 23 May 2023 08:19:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898aef05174dd44f95ded2cbc6b08ea0d2c217a6219cb0c6f3b2d90861943802`  
		Last Modified: Tue, 23 May 2023 08:19:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f257c14cb89d4f1884436c8bb608b9b23b0ec32d1ba0dd9699929e5df2397a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317076178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca296905ec313c4bbaf2509a896cee4410f0765d7b157dcb9cbdd3b756975df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:19 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 01:29:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:31:06 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Tue, 23 May 2023 01:31:06 GMT
WORKDIR /tmp
# Tue, 23 May 2023 01:31:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 23 May 2023 01:31:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 May 2023 01:31:20 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 01:31:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 01:31:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6f4a297b4e40485159fdaaaca21c302eba0567a5165c796f74cdfaaaeeefed`  
		Last Modified: Tue, 23 May 2023 01:37:02 GMT  
		Size: 191.4 MB (191387676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2554a6db7d9263fb78eec27ac142cb5603d75ef8ab2cb7a01cf8fcc881c57857`  
		Last Modified: Tue, 23 May 2023 01:38:00 GMT  
		Size: 72.0 MB (71994874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f752b58a03cf81ca21125b811888b8cebc87972c7dfcec999710b67e6ef55402`  
		Last Modified: Tue, 23 May 2023 01:37:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897d28fcb78920667bacdfa9a8f6ebff0c9f72a6fe0555c351580a0d5e996e5c`  
		Last Modified: Tue, 23 May 2023 01:37:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
