## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:f892a2b7959bf55be5249412f560d6f2338807a275608bb219613655bab57b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8c299c8c1624b4d1699221f1cf59f86651cd0104e19bd14794f5350536df5328
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308811882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c58741764a53feece954451e8ecfb7521ce501c2d11c436d0fe0d8bb90804b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Tue, 23 May 2023 08:09:53 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 08:09:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:09:53 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:09:59 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 08:09:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:09:59 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 08:10:16 GMT
RUN boot
# Tue, 23 May 2023 08:10:17 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 08:10:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 08:10:17 GMT
CMD ["repl"]
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
	-	`sha256:b84feaddbceda3af591163538831493ff2a82a2c307928e286aeba710c1800f5`  
		Last Modified: Tue, 23 May 2023 08:18:15 GMT  
		Size: 2.4 MB (2361679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d58c4b4ffd2e7bd6b020aeb49b2ff42c4503d13a53cfb10d4012ca94c15ceb`  
		Last Modified: Tue, 23 May 2023 08:18:18 GMT  
		Size: 58.8 MB (58820406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a51d40e31b47c9fd21e8c7d76d19a1650fed10cab44ad987d92e012a90f8482`  
		Last Modified: Tue, 23 May 2023 08:18:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d9cc765f875b3f472b38ad88c7c5577609f6f8c90e5cf5c7284311f83720d58f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306252244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed456089946e4d2833ed2a5f7102962bb8c445e4d3e3fc144177077788b12caa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Tue, 23 May 2023 01:29:23 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 01:29:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 01:29:23 GMT
WORKDIR /tmp
# Tue, 23 May 2023 01:29:28 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 01:29:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 01:29:28 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 01:29:45 GMT
RUN boot
# Tue, 23 May 2023 01:29:45 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 01:29:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 01:29:45 GMT
CMD ["repl"]
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
	-	`sha256:fcc7e1127f0bdff212b7d7fccce2e04e17e08ed54f53f50955c7bde469892a92`  
		Last Modified: Tue, 23 May 2023 01:36:51 GMT  
		Size: 2.4 MB (2351078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7681014644c2f634d8064cf457a8935999a653e8553624fcfe742f4647284a`  
		Last Modified: Tue, 23 May 2023 01:36:54 GMT  
		Size: 58.8 MB (58820478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecfc5407a3e71b919660ad2d8afc5740a417501d54517b118e1493f5fca1546`  
		Last Modified: Tue, 23 May 2023 01:36:51 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
