## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:c6804ff24e1e06501e28cbf109b185d731f81c94e3bd0470b6152b7fe4e6dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:26ab141d1e4ea678ff09040b1ec388eb13cf446e4c9ff1b67d32af8ec87d1e17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261065328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d94324f22f1bb9742065a5cec22898a92c4e7e90e842999927ccb1f051607c6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:37:07 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:37:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:37:08 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 03 Oct 2023 08:37:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 03 Oct 2023 08:37:09 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:37:16 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 03 Oct 2023 08:37:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Oct 2023 08:37:16 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 03 Oct 2023 08:37:35 GMT
RUN boot
# Tue, 03 Oct 2023 08:37:35 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16734f5ea39dcb28fc0915fa8b7c5206249856dfbec50b530c6e3ef0c0848a67`  
		Last Modified: Tue, 03 Oct 2023 08:53:55 GMT  
		Size: 144.8 MB (144825964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38ff7ccad4f5acd90aacecc23c71dd8088fe7488a9f1bc8220c6a60bc0655e7`  
		Last Modified: Tue, 03 Oct 2023 08:53:44 GMT  
		Size: 2.4 MB (2362115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6972c77d01580be079836165857b696b528af3b911c0e38f65048b1f125873`  
		Last Modified: Tue, 03 Oct 2023 08:53:47 GMT  
		Size: 58.8 MB (58820535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f8f872445075203439d62ac2ea47a23ab429fa60a9a08c09264b354ce57e351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256447359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7083bf01129150f6a99e882ca2c001bd83d99fe04d475522e175ce63a38abf4`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:20 GMT
ADD file:46dcdcde338d2c01fed5db3fac9041736d9305145d8fc2039dd5b3714d38ede8 in / 
# Wed, 20 Sep 2023 02:44:21 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:47:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:28:30 GMT
COPY dir:17ac9e9d4b4d03adb229076835643ca11e6db9d9c122779536bfc61364556722 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:28:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:28:34 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 03 Oct 2023 08:28:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 03 Oct 2023 08:28:34 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:28:40 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 03 Oct 2023 08:28:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Oct 2023 08:28:41 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 03 Oct 2023 08:28:58 GMT
RUN boot
# Tue, 03 Oct 2023 08:28:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:31f5dc1f52c865588c43d8ec718f14d430e149b28f0b28232da825da7ae28f76`  
		Last Modified: Wed, 20 Sep 2023 02:47:53 GMT  
		Size: 53.7 MB (53704892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a7b8a14c04002cf8b0bce5a27e74c505c88c8c88a87b2336daf00d7b70aabe`  
		Last Modified: Tue, 03 Oct 2023 08:38:25 GMT  
		Size: 141.6 MB (141570563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8927283b4afc871deb9ebce4bb763fd686142d3debd2b8a65db877df2332961`  
		Last Modified: Tue, 03 Oct 2023 08:38:17 GMT  
		Size: 2.4 MB (2351426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436fa48193d7c933971c678cba3f2d379127485a4fa1b7684f085c56e3031442`  
		Last Modified: Tue, 03 Oct 2023 08:38:20 GMT  
		Size: 58.8 MB (58820478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
